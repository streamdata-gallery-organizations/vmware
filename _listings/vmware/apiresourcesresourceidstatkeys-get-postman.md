{
  "info": {
    "name": "VMWare vRealize Operations Get StatKeys for Resource and Load var",
    "_postman_id": "a07d80f6-a833-4f7d-a264-b24e5581e309",
    "description": "Grabs CPU statKeys for a VM resource using the {{resourceId}} env var.\nPopulates two env vars:\ncpuStatKeys for GET stats for small requests (1 to ~10 VMs)\ncpuStatKeysJSON for POST stats for large requests (use in conjunction with {{resourceIds}}",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Resources",
      "item": [
        {
          "id": "621e09f4-55cf-422b-b979-dc2e09118642",
          "name": "ApiResourcesStatkeysByResourceIdGet2",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "suite-api",
                "api",
                "api/resources/:resourceId/statkeys"
              ],
              "variable": [
                {
                  "id": "resourceId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Grabs CPU statKeys for a VM resource using the {{resourceId}} env var.\nPopulates two env vars:\ncpuStatKeys for GET stats for small requests (1 to ~10 VMs)\ncpuStatKeysJSON for POST stats for large requests (use in conjunction with {{resourceIds}}"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "af046ec2-3a4e-49a0-a51e-73552ddaf917"
            }
          ]
        }
      ]
    }
  ]
}