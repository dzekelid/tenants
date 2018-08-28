{
  "info": {
    "name": "Predix Tenant Management Get tenant credentials",
    "_postman_id": "b7c7cf91-6419-41e0-86c0-891bc07a5869",
    "description": "Get tenant credentials .",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Tenant",
      "item": [
        {
          "id": "fc7522da-2b45-47c7-ae36-c6ce5454b8ab",
          "name": "getTenantCredentialsUsingGET",
          "request": {
            "url": "http://predix-tms.run.aws-usw02-pr.ice.predix.io/v1/client-credentials",
            "method": "GET",
            "header": [
              {
                "key": "TMS-Zone-Subdomain",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get tenant credentials ."
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "34bfa554-2342-418c-b894-0bcafbe54462"
            }
          ]
        }
      ]
    }
  ]
}