{
  "info": {
    "name": "Predix Event Audit Trail Delete Plugins Archive Tenants Archives",
    "_postman_id": "6194ab95-cbfc-4ccb-ba2e-6178099017b9",
    "description": "Delete plugins archive tenants archives.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Plugins",
      "item": [
        {
          "id": "09e1e184-ad9d-43fa-a0ef-ee33c50a342e",
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
              "id": "e19b1d5b-2d39-4e5b-b000-baed944bf59c"
            }
          ]
        },
        {
          "id": "11228d3a-74e4-464e-87e1-bf6d5762bd20",
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
              "id": "f38f36fb-908e-43af-8c10-190227f069e7"
            }
          ]
        },
        {
          "id": "00b0839a-4c12-4d1c-96a9-16afa71748b8",
          "name": "deleteV1PluginsArchiveTenantsTenantUuArchivesUu",
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
            "method": "DELETE",
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
            "description": "Delete plugins archive tenants archives."
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "e932a913-5d7c-4f42-9f95-f13ac9f6297a"
            }
          ]
        }
      ]
    }
  ]
}