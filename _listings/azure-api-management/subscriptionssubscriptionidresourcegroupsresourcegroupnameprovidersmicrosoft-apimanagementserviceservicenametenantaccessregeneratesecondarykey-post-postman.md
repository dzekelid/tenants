{
  "info": {
    "name": "Azure API Management API TenantAccess RegenerateSecondaryKey",
    "_postman_id": "2a5e9c82-25fe-4b17-8547-315a6d504d24",
    "description": "Regenerate secondary access key.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "tenants",
      "item": [
        {
          "id": "21165bd9-bdca-4e03-b6aa-a3d21f8b62dd",
          "name": "TenantAccess_RegenerateSecondaryKey",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.ApiManagement/service/:serviceName/tenant/access/regenerateSecondaryKey"
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
            "description": "Regenerate secondary access key"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cd2bad54-dcd4-452b-bf63-38b795f3ab66"
            }
          ]
        }
      ]
    }
  ]
}