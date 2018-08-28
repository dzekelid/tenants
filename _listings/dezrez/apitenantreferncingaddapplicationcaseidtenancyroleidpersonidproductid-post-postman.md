{
  "info": {
    "name": "Dezrez Creates a tenancy referencing application for a case using the details supplied",
    "_postman_id": "4a9448cc-3719-4fd3-bb6e-e3a86ce20821",
    "description": "Creates a tenancy referencing application for a case using the details supplied.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Creates",
      "item": [
        {
          "id": "99b51805-3922-45d5-bec3-602f207f311a",
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
              "id": "05d55c32-85c1-4839-94a7-b9f27f66fc09"
            }
          ]
        }
      ]
    },
    {
      "name": "S",
      "item": [
        {
          "id": "c6039d98-7a94-467d-a157-9484d39e0a2e",
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
              "id": "bef295fd-19cb-431f-8ad2-ca88e9c40e42"
            }
          ]
        },
        {
          "id": "46bdf2f1-4a4b-49f7-bfcf-afcf6f1bf1c6",
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
              "id": "679f7bb9-99c4-41db-bee8-761ebdb141cc"
            }
          ]
        }
      ]
    },
    {
      "name": "Submits",
      "item": [
        {
          "id": "c3967a6d-2942-4cd6-83f4-c22a5dd59e37",
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
              "id": "edd20106-ffad-46ef-9f54-624e74966525"
            }
          ]
        }
      ]
    }
  ]
}