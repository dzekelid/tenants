---
name: Azure Resource Manager
x-slug: azure-resource-manager
description: Azure Resource Manager enables you to deploy and manage the infrastructure
  for your Azure solutions. You organize related resources in resource groups, and
  deploy your resources with JSON templates. For an introduction to deploying and
  managing resources with Resource Manager, see Azure Resource Manager overview.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-resource-manager.png
x-kinRank: "8"
x-alexaRank: "0"
tags: Tenants
created: "2018-06-20"
modified: "2018-06-20"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/tenants/master/_listings/azure-resource-manager/apis.md
specificationVersion: "0.14"
apis:
- name: Azure Resource Manager API Tenants List
  x-api-slug: azure-resource-manager-api
  description: Gets the tenants for your account.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-resource-manager.png
  humanURL: https://docs.microsoft.com/en-us/rest/api/resources/
  baseURL: ://management.azure.com////tenants
  tags: Tenants
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/tenants/master/_listings/azure-resource-manager/tenants-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/tenants/master/_listings/azure-resource-manager/tenants-get-openapi.md
- name: Azure Resource Manager API
  x-api-slug: azure-resource-manager-api
  description: Azure Resource Manager enables you to deploy and manage the infrastructure
    for your Azure solutions. You organize related resources in resource groups, and
    deploy your resources with JSON templates. For an introduction to deploying and
    managing resources with Resource Manager, see Azure Resource Manager overview.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/azure-resource-manager.png
  humanURL: https://docs.microsoft.com/en-us/rest/api/resources/
  baseURL: ://management.azure.com//
  tags: Tenants
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/tenants/master/_listings/azure-resource-manager/openapi.md
x-common:
- type: x-website
  url: https://docs.microsoft.com/en-us/rest/api/resources/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---