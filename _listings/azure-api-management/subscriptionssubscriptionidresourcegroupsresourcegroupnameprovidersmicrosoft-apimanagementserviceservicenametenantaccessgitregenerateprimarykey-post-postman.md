{
  "info": {
    "name": "Azure API Management API TenantAccessGit RegeneratePrimaryKey",
    "_postman_id": "7bbf2e57-7088-40d2-9c32-13326782a9a7",
    "description": "Regenerate primary access key for GIT.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "tenants",
      "item": [
        {
          "id": "7d9efcaa-d7df-4046-93f4-5bb218fd3d36",
          "name": "TenantAccessGit_RegeneratePrimaryKey",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.ApiManagement/service/:serviceName/tenant/access/git/regeneratePrimaryKey"
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
            "description": "Regenerate primary access key for GIT"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f69bc851-cc4e-48f0-8454-95e6c4c04e7c"
            }
          ]
        }
      ]
    }
  ]
}