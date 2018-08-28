---
swagger: "2.0"
x-collection-name: Predix
x-complete: 0
info:
  title: Predix Event Audit Trail Delete Plugins Archive Tenants Archives
  description: Delete plugins archive tenants archives.
  version: 1.0.0
host: event-audit-trail.run.aws-usw02-pr.ice.predix.io
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v2/config/orchestrations/defaulttagquery:
    get:
      summary: Get the default tag query corresponding for the tenant.
      description: Returns all information (query string, fieldnamespecifier, tagnamespecifer,
        description etc.) associated with the default tag query. An error is returned
        if tag query does not exist for the tenant.
      operationId: retrieveDefaultTagQuery
      x-api-path-slug: apiv2configorchestrationsdefaulttagquery-get
      parameters:
      - in: header
        name: Authorization
        description: Authorization
      - in: header
        name: Predix-Zone-Id
        description: Predix-Zone-Id
      responses:
        200:
          description: Successful response
      tags:
      - Default
      - Tag
      - Query
      - Correspondingthe
      - Tenant
    post:
      summary: Create the default tag query corresponding for the tenant.
      description: Creates the default tag query including all information (query
        string, fieldnamespecifier, tagnamespecifer, description etc.) associated
        with the query.
      operationId: createDefaultTagQuery
      x-api-path-slug: apiv2configorchestrationsdefaulttagquery-post
      parameters:
      - in: header
        name: Authorization
        description: Authorization
      - in: body
        name: body
        description: tag names default query
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Predix-Zone-Id
        description: Predix-Zone-Id
      responses:
        200:
          description: Successful response
      tags:
      - Default
      - Tag
      - Query
      - Correspondingthe
      - Tenant
    put:
      summary: Update the default tag query for the tenant.
      description: Updates the default tag query including all information (query
        string, fieldnamespecifier, tagnamespecifer, description etc.) associated
        with the query.
      operationId: updateDefaultTagQuery
      x-api-path-slug: apiv2configorchestrationsdefaulttagquery-put
      parameters:
      - in: header
        name: Authorization
        description: Authorization
      - in: body
        name: body
        description: tag names default query
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Predix-Zone-Id
        description: Predix-Zone-Id
      responses:
        200:
          description: Successful response
      tags:
      - Default
      - Tag
      - Querythe
      - Tenant
    delete:
      summary: Delete the default tag query for the tenant.
      description: Deletes the default tag query.
      operationId: deleteDefaultTagQuery
      x-api-path-slug: apiv2configorchestrationsdefaulttagquery-delete
      parameters:
      - in: header
        name: Authorization
        description: Authorization
      - in: header
        name: Predix-Zone-Id
        description: Predix-Zone-Id
      responses:
        200:
          description: Successful response
      tags:
      - Default
      - Tag
      - Querythe
      - Tenant
  /provision/{tenantId}:
    delete:
      summary: deleteTenantConfig
      description: ""
      operationId: deleteTenantConfigUsingDELETE
      x-api-path-slug: provisiontenantid-delete
      parameters:
      - in: path
        name: tenantId
        description: tenantId
      responses:
        200:
          description: OK
      tags:
      - Provision
      - TenantId
  /v1/system/configs:
    get:
      summary: Get tenant-specific configuration settings
      description: This can be used to verify whether the audit feature is enabled.
      operationId: getV1SystemConfigs
      x-api-path-slug: v1systemconfigs-get
      responses:
        200:
          description: Successful response
      tags:
      - Tenant-specific
      - Configuration
      - Settings
    post:
      summary: Update tenant-specific configuration settings
      description: This can be used to enable or disable the audit feature.
      operationId: postV1SystemConfigs
      x-api-path-slug: v1systemconfigs-post
      parameters:
      - in: body
        name: body
        description: Array of configs to create
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: Successful response
      tags:
      - Tenant-specific
      - Configuration
      - Settings
  /v1/plugins/archive/tenants/{tenant_uuid}/archives:
    get:
      summary: Get Plugins Archive Tenants Archives
      description: Get plugins archive tenants archives.
      operationId: getV1PluginsArchiveTenantsTenantUuArchives
      x-api-path-slug: v1pluginsarchivetenantstenant-uuidarchives-get
      parameters:
      - in: path
        name: tenant_uuid
        description: tenant_uuid
      responses:
        200:
          description: Successful response
      tags:
      - Plugins
      - Archive
      - Tenants
      - Archives
  /v1/plugins/archive/tenants/{tenant_uuid}/archives/{uuid}:
    get:
      summary: Get Plugins Archive Tenants Archives
      description: Get plugins archive tenants archives.
      operationId: getV1PluginsArchiveTenantsTenantUuArchivesUu
      x-api-path-slug: v1pluginsarchivetenantstenant-uuidarchivesuuid-get
      parameters:
      - in: path
        name: tenant_uuid
        description: tenant_uuid
      - in: path
        name: uuid
        description: uuid
      responses:
        200:
          description: Successful response
      tags:
      - Plugins
      - Archive
      - Tenants
      - Archives
    delete:
      summary: Delete Plugins Archive Tenants Archives
      description: Delete plugins archive tenants archives.
      operationId: deleteV1PluginsArchiveTenantsTenantUuArchivesUu
      x-api-path-slug: v1pluginsarchivetenantstenant-uuidarchivesuuid-delete
      parameters:
      - in: path
        name: tenant_uuid
        description: tenant_uuid
      - in: path
        name: uuid
        description: uuid
      responses:
        200:
          description: Successful response
      tags:
      - Plugins
      - Archive
      - Tenants
      - Archives
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---