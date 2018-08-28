{
  "info": {
    "name": "Predix Event Audit Trail Get Plugins Archive Tenants Configuration",
    "_postman_id": "699b9e15-f668-41d7-b47a-afcd998b5f80",
    "description": "Get plugins archive tenants configuration.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Plugins",
      "item": [
        {
          "id": "4faeb402-984a-4ec6-af8b-1bc0df3a413a",
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
              "id": "908bd8e0-bf53-4950-aef4-cd5e2e66ef22"
            }
          ]
        },
        {
          "id": "2067506a-2d79-4262-a895-660f7895a792",
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
              "id": "9e320e1d-69ba-406a-9a0e-ccacca9aa68b"
            }
          ]
        },
        {
          "id": "b53d155b-34e9-4269-be10-737c207ee31a",
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
              "id": "1c6ddd98-6005-4997-b505-5de86bd2d113"
            }
          ]
        },
        {
          "id": "a5d7f30c-f813-47aa-a0aa-8b38d6c27f3a",
          "name": "getV1PluginsArchiveTenantsTenantUuConfiguration",
          "request": {
            "url": {
              "protocol": "http",
              "host": "event-audit-trail.run.aws-usw02-pr.ice.predix.io",
              "path": [
                "v1/plugins/archive/tenants/:tenant_uuid/configuration"
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
            "description": "Get plugins archive tenants configuration."
          },
          "response": [
            {
              "status": "Successful response",
              "code": 200,
              "name": "Response_200",
              "id": "e1b9aad6-4d12-42e8-a197-913c5a67c8a8"
            }
          ]
        }
      ]
    }
  ]
}