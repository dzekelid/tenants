{
  "info": {
    "name": "Dezrez Adds a Guarantor to a tenancy referencing application for a case using the details supplied",
    "_postman_id": "c57fe111-107f-4331-b9e9-e0fa0cd2c23d",
    "description": "Adds a guarantor to a tenancy referencing application for a case using the details supplied.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Creates",
      "item": [
        {
          "id": "e9b41cac-bcba-420f-9622-e8e2f5912666",
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
              "id": "b2788188-e41b-4967-aa60-20dc62b35367"
            }
          ]
        }
      ]
    },
    {
      "name": "S",
      "item": [
        {
          "id": "f716475a-12c0-48fa-96ca-40dd4822a7c2",
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
              "id": "611cd627-7ac2-4340-b1cd-ecda6a161c86"
            }
          ]
        },
        {
          "id": "d8daac76-3eca-428b-b294-23b83e1d0a74",
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
              "id": "5d68410b-668e-4730-8dd3-31504fbc74a7"
            }
          ]
        }
      ]
    },
    {
      "name": "Submits",
      "item": [
        {
          "id": "1ce08b9e-f3af-4b22-91b1-25d6f5806738",
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
              "id": "cba86273-d1c4-4044-94ff-d75d3b7ce783"
            }
          ]
        }
      ]
    }
  ]
}