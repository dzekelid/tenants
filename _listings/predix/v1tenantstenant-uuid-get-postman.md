{
  "info": {
    "name": "Predix Notification Service Get Tenants",
    "_postman_id": "acf8e8b2-24ee-4bb0-b534-ac476e2a23ce",
    "description": "Get tenants.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Tenants",
      "item": [
        {
          "id": "2648e30e-9db7-459a-90fe-c5f686fdf895",
          "name": "getV1TenantsTenantUu",
          "request": {
            "url": {
              "protocol": "http",
              "host": "ev-notification-service.run.aws-usw02-pr.ice.predix.io",
              "path": [
                "v1/tenants/:tenant_uuid"
              ],
              "variable": [
                {
                  "id": "tenant_uuid",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get tenants."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1926b7a1-7ae9-40bf-8fc6-c3266684d5c4"
            }
          ]
        }
      ]
    }
  ]
}