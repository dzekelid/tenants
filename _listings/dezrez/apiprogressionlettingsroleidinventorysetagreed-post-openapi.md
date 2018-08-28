---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Sets whether inventory is agreed with tenants
  version: 1.0.0
  description: Sets whether inventory is agreed with tenants.
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/progression/lettings/{roleId}/inventory/setagreed:
    post:
      summary: Sets whether inventory is agreed with tenants
      description: Sets whether inventory is agreed with tenants.
      operationId: LettingsProgression_SetInventoryAgreedByroleIdByagreed
      x-api-path-slug: apiprogressionlettingsroleidinventorysetagreed-post
      parameters:
      - in: query
        name: agreed
        description: Is inventory agreed
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: roleId
        description: Tenant role id
      responses:
        200:
          description: OK
      tags:
      - Sets
      - Whether
      - Inventory
      - Is
      - Agreed
      - Tenants
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