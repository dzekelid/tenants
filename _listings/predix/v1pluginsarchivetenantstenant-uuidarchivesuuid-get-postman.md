{
  "info": {
    "name": "Predix Event Audit Trail Get Plugins Archive Tenants Archives",
    "_postman_id": "6469fc40-ee03-425d-a37b-21b91c3682b8",
    "description": "Get plugins archive tenants archives.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Plugins",
      "item": [
        {
          "id": "f9f65ba3-3b72-4aef-a7b4-330d67e821a3",
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
              "id": "183a101b-1344-4de8-a3c2-70814335b473"
            }
          ]
        },
        {
          "id": "d608976e-d291-4889-9485-45c714a43f64",
          "name": "getV1PluginsArchiveTenantsTenantUuArchivesUu",
          "request": {
            "url": {
              "protocol": "http",
              "host": "event-audit-trail.run.aws-usw02-pr.ice.predix.io",
              "path": [
                "v1/plugins/archive/tenants/:tenant_uuid/archives/:uuid"
              ],
              "variable": [
                {
                  "id": "tenant_uuid",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "uuid",
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
              "id": "090da17b-9137-44e4-9d45-fab2e89b1cea"
            }
          ]
        }
      ]
    }
  ]
}