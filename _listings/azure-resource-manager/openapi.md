swagger: "2.0"
x-collection-name: Azure Resource Manager
x-complete: 1
info:
  title: SubscriptionClient
  description: all-resource-groups-and-resources-exist-within-subscriptions--these-operation-enable-you-get-information-about-your-subscriptions-and-tenants--a-tenant-is-a-dedicated-instance-of-azure-active-directory-azure-ad-for-your-organization-
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /tenants:
    get:
      summary: Tenants List
      description: Gets the tenants for your account.
      operationId: Tenants_List
      x-api-path-slug: tenants-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Tenants