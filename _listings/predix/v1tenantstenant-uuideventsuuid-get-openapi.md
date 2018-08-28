---
swagger: "2.0"
x-collection-name: Predix
x-complete: 0
info:
  title: Predix Event Audit Trail Get Tenants Events
  description: Get tenants events.
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
  /v1/plugins/archive/tenants/{tenant_uuid}/configuration:
    get:
      summary: Get Plugins Archive Tenants Configuration
      description: Get plugins archive tenants configuration.
      operationId: getV1PluginsArchiveTenantsTenantUuConfiguration
      x-api-path-slug: v1pluginsarchivetenantstenant-uuidconfiguration-get
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
      - Configuration
    post:
      summary: Post Plugins Archive Tenants Configuration
      description: Post plugins archive tenants configuration.
      operationId: postV1PluginsArchiveTenantsTenantUuConfiguration
      x-api-path-slug: v1pluginsarchivetenantstenant-uuidconfiguration-post
      parameters:
      - in: body
        name: archivePluginConfiguration
        description: archivePluginConfiguration
        schema:
          $ref: '#/definitions/holder'
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
      - Configuration
  /v1/plugins/archive/tenants/{tenant_uuid}/staged-events:
    get:
      summary: Get Plugins Archive Tenants Staged Events
      description: Get plugins archive tenants staged events.
      operationId: getV1PluginsArchiveTenantsTenantUuStagedEvents
      x-api-path-slug: v1pluginsarchivetenantstenant-uuidstagedevents-get
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
      - Staged
      - Events
  /v1/tenants/{tenant_uuid}:
    get:
      summary: Get Tenants
      description: Get tenants.
      operationId: getV1TenantsTenantUu
      x-api-path-slug: v1tenantstenant-uuid-get
      parameters:
      - in: path
        name: tenant_uuid
        description: tenant_uuid
      responses:
        200:
          description: Successful response
      tags:
      - Tenants
  /v1/tenants/{tenant_uuid}/event-search:
    get:
      summary: Get Tenants Event Search
      description: Get tenants event search.
      operationId: getV1TenantsTenantUuEventSearch
      x-api-path-slug: v1tenantstenant-uuideventsearch-get
      parameters:
      - in: query
        name: query
        description: query
      - in: path
        name: tenant_uuid
        description: tenant_uuid
      responses:
        200:
          description: Successful response
      tags:
      - Tenants
      - Event
      - Search
  /v1/tenants/{tenant_uuid}/events:
    get:
      summary: Get Tenants Events
      description: Get tenants events.
      operationId: getV1TenantsTenantUuEvents
      x-api-path-slug: v1tenantstenant-uuidevents-get
      parameters:
      - in: query
        name: classification
        description: classification
      - in: query
        name: context
        description: context
      - in: query
        name: end_date
        description: end_date
      - in: query
        name: start_date
        description: start_date
      - in: query
        name: tag
        description: tag
      - in: path
        name: tenant_uuid
        description: tenant_uuid
      responses:
        200:
          description: Successful response
      tags:
      - Tenants
      - Events
    post:
      summary: Post Tenants Events
      description: Post tenants events.
      operationId: postV1TenantsTenantUuEvents
      x-api-path-slug: v1tenantstenant-uuidevents-post
      parameters:
      - in: body
        name: events
        description: events
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: tenant_uuid
        description: tenant_uuid
      responses:
        200:
          description: Successful response
      tags:
      - Tenants
      - Events
  /v1/tenants/{tenant_uuid}/events/{uuid}:
    get:
      summary: Get Tenants Events
      description: Get tenants events.
      operationId: getV1TenantsTenantUuEventsUu
      x-api-path-slug: v1tenantstenant-uuideventsuuid-get
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
      - Tenants
      - Events
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