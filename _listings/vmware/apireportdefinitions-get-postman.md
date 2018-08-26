{
  "info": {
    "name": "VMWare vRealize Operations Get Report Definitions",
    "_postman_id": "4e5fb17f-7bc0-439d-a151-07633899f818",
    "description": "Gets all - to get a single report ID, just add /<report def id>",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Reportdefinitions",
      "item": [
        {
          "id": "053f1bf5-ae9d-4c01-b9bd-7f412a757648",
          "name": "ApiReportdefinitionsGet",
          "request": {
            "url": "http://example.com/suite-api/api/api/reportdefinitions",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Content-Type",
                "value": "{}",
                "description": "",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Gets all - to get a single report ID, just add /<report def id>"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1601b8c6-47f2-4e2d-aa57-82d414c90bf4"
            }
          ]
        }
      ]
    }
  ]
}