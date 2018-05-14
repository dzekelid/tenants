{
  "info": {
    "name": "Azure API Management API TenantAccessGit Get",
    "_postman_id": "7d3f6854-cc22-4821-b8cf-7513d2c5c5c6",
    "description": "Gets the Git access configuration for the tenant.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "tenants",
      "item": [
        {
          "id": "22a4dddb-780c-4e96-9e67-2e536e45bb35",
          "name": "TenantAccessGit_Get",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.ApiManagement/service/:serviceName/tenant/access/git"
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
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the Git access configuration for the tenant"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "18b3b0bc-62d7-4b25-b35e-e582a09e2fe9"
            }
          ]
        }
      ]
    }
  ]
}