{
  "info": {
    "name": "Azure API Management API TenantAccessGit RegenerateSecondaryKey",
    "_postman_id": "4c92ca36-455a-49ba-b083-203b1b44e714",
    "description": "Regenerate secondary access key for GIT.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "tenants",
      "item": [
        {
          "id": "5539f573-7da2-4e78-8faa-b6d2a7602522",
          "name": "TenantAccessGit_RegenerateSecondaryKey",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.ApiManagement/service/:serviceName/tenant/access/git/regenerateSecondaryKey"
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
            "description": "Regenerate secondary access key for GIT"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e02f9496-7083-4743-a4e5-f0e18f3917c3"
            }
          ]
        }
      ]
    }
  ]
}