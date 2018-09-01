{
  "info": {
    "name": "VMWare vRealize Operations Get Generated Reports",
    "_postman_id": "a00ee4bb-3b53-42c2-ad46-a672591c1ed9",
    "description": "You can check status of report runs this way.\nTo get a specific generated report add /<report id>",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Reports",
      "item": [
        {
          "id": "810ab968-1192-417e-9c71-1aa802adea0c",
          "name": "ApiReportsGet",
          "request": {
            "url": "http://example.com/suite-api/api/api/reports",
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
            "description": "You can check status of report runs this way.\nTo get a specific generated report add /<report id>"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "afeb7f67-8696-4889-8340-9a18e2f73b6b"
            }
          ]
        }
      ]
    }
  ]
}