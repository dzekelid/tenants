{
  "info": {
    "name": "Dezrez Gets all tenancy referencing applications for the caseId provided",
    "_postman_id": "5cd9da86-ca51-406b-942c-bbe3ba81b5a1",
    "description": "Gets all tenancy referencing applications for the caseid provided.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Creates",
      "item": [
        {
          "id": "eefc6ecb-06b4-4b49-a5dc-648e0ad6be5b",
          "name": "TenantReferencing_CreateApplicationBycaseIdBytenancyRoleIdBypersonIdByproductId",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.dezrez.com",
              "path": [
                "api/tenantreferncing/addapplication/:caseId/:tenancyRoleId/:personId/:productId"
              ],
              "variable": [
                {
                  "id": "caseId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "personId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "productId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "tenancyRoleId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "header": [
              {
                "key": "Rezi-Api-Version",
                "value": "{}",
                "description": "Specifies which version of the API to call",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Creates a tenancy referencing application for a case using the details supplied."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "be400489-2f25-47db-a218-4780e60237a8"
            }
          ]
        }
      ]
    },
    {
      "name": "S",
      "item": [
        {
          "id": "81b64fd2-615f-4005-a5e0-93be98729e47",
          "name": "TenantReferencing_CreateApplicationBycaseIdBytenancyRoleIdBypersonId",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.dezrez.com",
              "path": [
                "api/tenantreferncing/addguarantor/:caseId/:tenancyRoleId/:personId"
              ],
              "variable": [
                {
                  "id": "caseId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "personId",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "tenancyRoleId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "header": [
              {
                "key": "Rezi-Api-Version",
                "value": "{}",
                "description": "Specifies which version of the API to call",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Adds a guarantor to a tenancy referencing application for a case using the details supplied."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "19197bbb-4e9b-4faa-ac5a-f4df73770c13"
            }
          ]
        },
        {
          "id": "64e2ba53-6a5d-426c-afe1-662ae657ea68",
          "name": "TenantReferencing_GetApplicationsBycaseId",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.dezrez.com",
              "path": [
                "api/tenantreferncing/applications/:caseId"
              ],
              "variable": [
                {
                  "id": "caseId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Rezi-Api-Version",
                "value": "{}",
                "description": "Specifies which version of the API to call",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Gets all tenancy referencing applications for the caseid provided."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3843a452-9ecc-48a8-959d-12f51b849244"
            }
          ]
        }
      ]
    },
    {
      "name": "Submits",
      "item": [
        {
          "id": "b4fafdb5-7fa7-45f5-b1f0-230f36741cbe",
          "name": "TenantReferencing_SubmitApplicationForReferencingBycaseId",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.dezrez.com",
              "path": [
                "api/tenantreferncing/submitapplication/:caseId"
              ],
              "variable": [
                {
                  "id": "caseId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "PUT",
            "header": [
              {
                "key": "Rezi-Api-Version",
                "value": "{}",
                "description": "Specifies which version of the API to call",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Submits an individual referencing application for processing."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1acb1b04-a04d-4e1a-8d7f-8df317bafb0f"
            }
          ]
        }
      ]
    }
  ]
}