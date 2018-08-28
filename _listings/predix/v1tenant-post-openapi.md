---
swagger: "2.0"
x-collection-name: Predix
x-complete: 0
info:
  title: Predix Tenant Management create a tenant
  description: Create a tenant.
  version: 1.0.0
host: predix-tms.run.aws-usw02-pr.ice.predix.io
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
          description: OK
      tags:
      - Tenants
    put:
      summary: Put Tenants
      description: Put tenants.
      operationId: putV1TenantsTenantUu
      x-api-path-slug: v1tenantstenant-uuid-put
      parameters:
      - in: body
        name: tenant
        description: tenant
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: tenant_uuid
        description: tenant_uuid
      responses:
        200:
          description: OK
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
          description: OK
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
    put:
      summary: Put Tenants Events
      description: Put tenants events.
      operationId: putV1TenantsTenantUuEventsUu
      x-api-path-slug: v1tenantstenant-uuideventsuuid-put
      parameters:
      - in: body
        name: event
        description: event
        schema:
          $ref: '#/definitions/holder'
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
    delete:
      summary: Delete Tenants Events
      description: Delete tenants events.
      operationId: deleteV1TenantsTenantUuEventsUu
      x-api-path-slug: v1tenantstenant-uuideventsuuid-delete
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
  /v1/tenants/{tenant_uuid}/configurations:
    get:
      summary: Get Tenants Configurations
      description: Get tenants configurations.
      operationId: getV1TenantsTenantUuConfigurations
      x-api-path-slug: v1tenantstenant-uuidconfigurations-get
      parameters:
      - in: query
        name: configurationUuid
        description: configurationUuid
      - in: path
        name: tenant_uuid
        description: tenant_uuid
      responses:
        200:
          description: OK
      tags:
      - Tenants
      - Configurations
    post:
      summary: Post Tenants Configurations
      description: Post tenants configurations.
      operationId: postV1TenantsTenantUuConfigurations
      x-api-path-slug: v1tenantstenant-uuidconfigurations-post
      parameters:
      - in: body
        name: configurations
        description: configurations
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: tenant_uuid
        description: tenant_uuid
      responses:
        200:
          description: OK
      tags:
      - Tenants
      - Configurations
  /v1/tenants/{tenant_uuid}/configurations/{uuid}:
    get:
      summary: Get Tenants Configurations
      description: Get tenants configurations.
      operationId: getV1TenantsTenantUuConfigurationsUu
      x-api-path-slug: v1tenantstenant-uuidconfigurationsuuid-get
      parameters:
      - in: path
        name: tenant_uuid
        description: tenant_uuid
      - in: path
        name: uuid
        description: uuid
      responses:
        200:
          description: OK
      tags:
      - Tenants
      - Configurations
    put:
      summary: Put Tenants Configurations
      description: Put tenants configurations.
      operationId: putV1TenantsTenantUuConfigurationsUu
      x-api-path-slug: v1tenantstenant-uuidconfigurationsuuid-put
      parameters:
      - in: body
        name: configuration
        description: configuration
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: tenant_uuid
        description: tenant_uuid
      - in: path
        name: uuid
        description: uuid
      responses:
        200:
          description: OK
      tags:
      - Tenants
      - Configurations
    delete:
      summary: Delete Tenants Configurations
      description: Delete tenants configurations.
      operationId: deleteV1TenantsTenantUuConfigurationsUu
      x-api-path-slug: v1tenantstenant-uuidconfigurationsuuid-delete
      parameters:
      - in: path
        name: tenant_uuid
        description: tenant_uuid
      - in: path
        name: uuid
        description: uuid
      responses:
        200:
          description: OK
      tags:
      - Tenants
      - Configurations
  /v1/tenants/{tenant_uuid}/email:
    post:
      summary: Post Tenants Email
      description: Post tenants email.
      operationId: postV1TenantsTenantUuEmail
      x-api-path-slug: v1tenantstenant-uuidemail-post
      parameters:
      - in: body
        name: applicationMessage
        description: applicationMessage
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: configuration
        description: configuration
      - in: path
        name: tenant_uuid
        description: tenant_uuid
      responses:
        200:
          description: OK
      tags:
      - Tenants
      - Email
  /v1/tenants/{tenant_uuid}/usage:
    get:
      summary: Get Tenants Usage
      description: Get tenants usage.
      operationId: getV1TenantsTenantUuUsage
      x-api-path-slug: v1tenantstenant-uuidusage-get
      parameters:
      - in: query
        name: end_date
        description: end_date
      - in: query
        name: start_date
        description: start_date
      - in: path
        name: tenant_uuid
        description: tenant_uuid
      responses:
        200:
          description: OK
      tags:
      - Tenants
      - Usage
  /v1/tenant:
    get:
      summary: Retrieve all the tenants in the given zone
      description: Retrieve all the tenants in the given zone.
      operationId: getTenantsUsingGET
      x-api-path-slug: v1tenant-get
      parameters:
      - in: header
        name: Predix-Zone-Id
      responses:
        200:
          description: Successful response
      tags:
      - Retrieve
      - ""
      - Tenants
      - In
      - Given
      - Zone
    post:
      summary: create a tenant
      description: Create a tenant.
      operationId: createTenantUsingPOST
      x-api-path-slug: v1tenant-post
      parameters:
      - in: header
        name: Predix-Zone-Id
      - in: body
        name: tenantProvisioningRequest
        description: tenantProvisioningRequest
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: Successful response
      tags:
      - Create
      - Tenant
    put:
      summary: update a tenant
      description: Update a tenant.
      operationId: updateTenantUsingPUT
      x-api-path-slug: v1tenant-put
      parameters:
      - in: header
        name: Predix-Zone-Id
      - in: body
        name: tenantProvisioningRequest
        description: tenantProvisioningRequest
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: Successful response
      tags:
      - Update
      - Tenant
  /v1/tenant/{tenantName}/status:
    get:
      summary: Retrieve a tenant's status
      description: Retrieve a tenant's status.
      operationId: getTenantStatusUsingGET
      x-api-path-slug: v1tenanttenantnamestatus-get
      parameters:
      - in: header
        name: Predix-Zone-Id
      - in: path
        name: tenantName
        description: tenantName
      responses:
        200:
          description: Successful response
      tags:
      - Retrieve
      - Tenants
      - Status
  /v1/client-credentials:
    get:
      summary: Get tenant credentials
      description: Get tenant credentials .
      operationId: getTenantCredentialsUsingGET
      x-api-path-slug: v1clientcredentials-get
      parameters:
      - in: header
        name: TMS-Zone-Subdomain
      responses:
        200:
          description: Successful response
      tags:
      - Tenant
      - Credentials
    post:
      summary: Create tenant credentials
      description: Create tenant credentials .
      operationId: createTenantCredentialsUsingPOST
      x-api-path-slug: v1clientcredentials-post
      parameters:
      - in: body
        name: tenantCredentialsRequests
        description: tenantCredentialsRequests
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: TMS-Zone-Subdomain
      responses:
        200:
          description: Successful response
      tags:
      - Tenant
      - Credentials
    put:
      summary: Create tenant credentials
      description: Create tenant credentials .
      operationId: updateTenantCredentialsUsingPUT
      x-api-path-slug: v1clientcredentials-put
      parameters:
      - in: body
        name: tenantCredentialsRequest
        description: tenantCredentialsRequest
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: TMS-Zone-Subdomain
      responses:
        200:
          description: Successful response
      tags:
      - Tenant
      - Credentials
  /v1/client-credentials/client-ids/{clientId}:
    delete:
      summary: Delete tenant credentials
      description: Delete tenant credentials .
      operationId: deleteTenantCredentialsUsingDELETE_1
      x-api-path-slug: v1clientcredentialsclientidsclientid-delete
      parameters:
      - in: path
        name: clientId
        description: clientId
      - in: header
        name: TMS-Zone-Subdomain
      responses:
        200:
          description: Successful response
      tags:
      - Tenant
      - Credentials
  /v1/client-credentials/client-ids/{clientId}/authorized-clients/{authorizedClientId}:
    delete:
      summary: Delete tenant credentials
      description: Delete tenant credentials .
      operationId: deleteTenantCredentialsUsingDELETE
      x-api-path-slug: v1clientcredentialsclientidsclientidauthorizedclientsauthorizedclientid-delete
      parameters:
      - in: path
        name: authorizedClientId
        description: authorizedClientId
      - in: path
        name: clientId
        description: clientId
      - in: header
        name: TMS-Zone-Subdomain
      responses:
        200:
          description: Successful response
      tags:
      - Tenant
      - Credentials
  /v1/tenant/profile:
    get:
      summary: Lookup Tenant by Subdomain
      description: Lookup tenant by subdomain.
      operationId: getTenantBySubdomainUsingGET
      x-api-path-slug: v1tenantprofile-get
      parameters:
      - in: header
        name: TMS-Zone-Subdomain
      responses:
        200:
          description: Successful response
      tags:
      - Lookup
      - Tenant
      - By
      - Subdomain
  /v1/tenant/profile/service/{serviceName}:
    get:
      summary: Lookup Tenant service by Subdomain
      description: Lookup tenant service by subdomain.
      operationId: getTenantServiceBySubdomainUsingGET
      x-api-path-slug: v1tenantprofileserviceservicename-get
      parameters:
      - in: path
        name: serviceName
        description: serviceName
      - in: header
        name: TMS-Zone-Subdomain
      responses:
        200:
          description: Successful response
      tags:
      - Lookup
      - Tenant
      - Service
      - By
      - Subdomain
  /v1/tenant/{tenantName}:
    get:
      summary: Retrieve a tenant and its list of services
      description: Retrieve a tenant and its list of services.
      operationId: getTenantUsingGET
      x-api-path-slug: v1tenanttenantname-get
      parameters:
      - in: header
        name: Predix-Zone-Id
      - in: path
        name: tenantName
        description: tenantName
      responses:
        200:
          description: Successful response
      tags:
      - Retrieve
      - Tenant
      - Its
      - List
      - Of
      - Services
  /v1/tenant/{tenantname}:
    delete:
      summary: Delete a tenant
      description: Delete a tenant.
      operationId: deleteTenantUsingDELETE
      x-api-path-slug: v1tenanttenantname-delete
      parameters:
      - in: header
        name: Predix-Zone-Id
      - in: path
        name: tenantname
        description: tenantName
      responses:
        200:
          description: Successful response
      tags:
      - Tenant
  /v2/tenants/{tenantSubdomain}:
    get:
      summary: Lookup Tenant by Subdomain
      description: Lookup tenant by subdomain.
      operationId: getTenantProfileBySubdomainUsingGET
      x-api-path-slug: v2tenantstenantsubdomain-get
      parameters:
      - in: path
        name: tenantSubdomain
        description: tenantSubdomain
      responses:
        200:
          description: Successful response
      tags:
      - Lookup
      - Tenant
      - By
      - Subdomain
    put:
      summary: Create or Update Tenant by Subdomain
      description: Create or update tenant by subdomain.
      operationId: upsertTenantBySubdomainUsingPUT
      x-api-path-slug: v2tenantstenantsubdomain-put
      parameters:
      - in: body
        name: tenantProfile
        description: tenantProfile
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: tenantSubdomain
        description: tenantSubdomain
      responses:
        200:
          description: Successful response
      tags:
      - Tenant
      - By
      - Subdomain
    delete:
      summary: Delete Tenant by Subdomain
      description: Delete tenant by subdomain.
      operationId: deleteTenantBySubdomainUsingDELETE
      x-api-path-slug: v2tenantstenantsubdomain-delete
      parameters:
      - in: path
        name: tenantSubdomain
        description: tenantSubdomain
      responses:
        200:
          description: Successful response
      tags:
      - Tenant
      - By
      - Subdomain
  /v2/tenants/{tenantSubdomain}/service-instances/{serviceInstanceName}:
    get:
      summary: Lookup Tenant Service by Subdomain
      description: Lookup tenant service by subdomain.
      operationId: getTenantServiceBySubdomainUsingGET_1
      x-api-path-slug: v2tenantstenantsubdomainserviceinstancesserviceinstancename-get
      parameters:
      - in: path
        name: serviceInstanceName
        description: serviceInstanceName
      - in: path
        name: tenantSubdomain
        description: tenantSubdomain
      responses:
        200:
          description: Successful response
      tags:
      - Lookup
      - Tenant
      - Service
      - By
      - Subdomain
    put:
      summary: Update Tenant Service by Subdomain
      description: Update tenant service by subdomain.
      operationId: upsertTenantServiceUsingPUT
      x-api-path-slug: v2tenantstenantsubdomainserviceinstancesserviceinstancename-put
      parameters:
      - in: path
        name: serviceInstanceName
        description: serviceInstanceName
      - in: body
        name: serviceRequest
        description: serviceRequest
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: tenantSubdomain
        description: tenantSubdomain
      responses:
        200:
          description: Successful response
      tags:
      - Tenant
      - Service
      - By
      - Subdomain
    delete:
      summary: Delete Tenant Service by Subdomain
      description: Delete tenant service by subdomain.
      operationId: deleteTenantServiceInstanceUsingDELETE
      x-api-path-slug: v2tenantstenantsubdomainserviceinstancesserviceinstancename-delete
      parameters:
      - in: path
        name: serviceInstanceName
        description: serviceInstanceName
      - in: path
        name: tenantSubdomain
        description: tenantSubdomain
      responses:
        200:
          description: Successful response
      tags:
      - Tenant
      - Service
      - By
      - Subdomain
  /v2/tenants/{tenantSubdomain}/status:
    get:
      summary: Lookup Tenant status by Subdomain
      description: Lookup tenant status by subdomain.
      operationId: getTenantProfileStatusBySubdomainUsingGET
      x-api-path-slug: v2tenantstenantsubdomainstatus-get
      parameters:
      - in: path
        name: tenantSubdomain
        description: tenantSubdomain
      responses:
        200:
          description: Successful response
      tags:
      - Lookup
      - Tenant
      - Status
      - By
      - Subdomain
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