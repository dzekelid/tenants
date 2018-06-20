{
  "info": {
    "name": "Azure API Management API TenantConfigurationSyncState Get",
    "_postman_id": "c767ae62-76db-4e27-8065-a11b01f0f367",
    "description": "Gets the status of the most recent synchronization between the configuration database and the Git repository.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "tenants",
      "item": [
        {
          "id": "0f1db3a6-639a-4387-b3e9-4bbc5851f05f",
          "name": "TenantConfigurationSyncState_Get",
          "request": {
            "url": {
              "protocol": "http",
              "host": "management.azure.com",
              "path": [
                "subscriptions/:subscriptionId/resourceGroups/:resourceGroupName/providers/Microsoft.ApiManagement/service/:serviceName/tenant/configuration/syncState"
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
            "description": "Gets the status of the most recent synchronization between the configuration database and the Git repository"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "43e1efb7-7da7-4a0d-8140-e693e2587e4e"
            }
          ]
        }
      ]
    }
  ]
}