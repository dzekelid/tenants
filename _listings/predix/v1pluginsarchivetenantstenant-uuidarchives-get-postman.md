{
  "info": {
    "name": "Predix Event Audit Trail Get Plugins Archive Tenants Archives",
    "_postman_id": "c64217a4-39af-4a7a-80eb-cc4c9126b586",
    "description": "Get plugins archive tenants archives.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Plugins",
      "item": [
        {
          "id": "9b4a6f2b-3c37-4fe8-96a7-0281ee113f6e",
          "name": "getV1PluginsArchiveTenantsTenantUuArchives",
          "request": {
            "url": {
              "protocol": "http",
              "host": "event-audit-trail.run.aws-usw02-pr.ice.predix.io",
              "path": [
                "v1/plugins/archive/tenants/:tenant_uuid/archives"
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
            "description": "Get plugins archive tenants archives."
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "7d6da96c-089a-4cc9-878e-5f40cbbfb94f"
            }
          ]
        }
      ]
    }
  ]
}