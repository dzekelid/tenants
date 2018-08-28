{
  "info": {
    "name": "Azure API Management API TenantAccess RegeneratePrimaryKey",
    "_postman_id": "7f8bd366-5c58-435f-ac67-b0aa2cdb0ed0",
    "description": "Regenerate primary access key.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "tenants",
      "item": [
        {
          "id": "6314296c-0fae-4419-8ee0-c82b4c5f95ae",
          "name": "TenantAccess_RegeneratePrimaryKey",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.ApiManagement/service/:serviceName/tenant/access/regeneratePrimaryKey"
              ],
              "query": [
                {
                  "key": "No Name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "subscriptionId",
                  "value": "subscriptionId",
                  "type": "string"
                },
                {
                  "id": "resourceGroupName",
                  "value": "resourceGroupName",
                  "type": "string"
                },
                {
                  "id": "serviceName",
                  "value": "serviceName",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Regenerate primary access key"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "43f405bc-1dcb-41db-bc47-3b7d9873da6d"
            }
          ]
        }
      ]
    }
  ]
}