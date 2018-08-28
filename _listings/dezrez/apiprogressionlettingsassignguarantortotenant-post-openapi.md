---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Assign guarantor to a tenant and vice versa
  version: 1.0.0
  description: Assign guarantor to a tenant and vice versa.
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
  /api/progression/lettings/{id}/setguaranteedrent:
    post:
      summary: Set the guaranteed rent a landlord will receive for a roles tenancies
      description: Set the guaranteed rent a landlord will receive for a roles tenancies.
      operationId: LettingsProgression_SetGuaranteedRentByidByamount
      x-api-path-slug: apiprogressionlettingsidsetguaranteedrent-post
      parameters:
      - in: query
        name: amount
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Set
      - Guaranteed
      - Rent
      - Landlord
      - Will
      - Receivea
      - Roles
      - Tenancies
  /api/documentgeneration/tenancyagreementast:
    post:
      summary: Generates Tenancy Agreement correspondence
      description: Generates tenancy agreement correspondence.
      operationId: DocumentGeneration_TenancyAgreementASTBygeneratePackDetails
      x-api-path-slug: apidocumentgenerationtenancyagreementast-post
      parameters:
      - in: body
        name: generatePackDetails
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Generates
      - Tenancy
      - Agreement
      - Correspondence
  /api/documentgeneration/tenancyguarantor:
    post:
      summary: Generates Tenancy Guarantor correspondence
      description: Generates tenancy guarantor correspondence.
      operationId: DocumentGeneration_TenancyGuarantorBygeneratePackDetails
      x-api-path-slug: apidocumentgenerationtenancyguarantor-post
      parameters:
      - in: body
        name: generatePackDetails
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Generates
      - Tenancy
      - Guarantor
      - Correspondence
  /api/role/lettings/{id}/removeadditionalservice/{additionalServiceId}:
    post:
      summary: Remove additional service to lettings role tenancy
      description: Remove additional service to lettings role tenancy.
      operationId: LettingRole_DeleteAdditionalServiceByidByadditionalServiceId
      x-api-path-slug: apirolelettingsidremoveadditionalserviceadditionalserviceid-post
      parameters:
      - in: path
        name: additionalServiceId
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Additional
      - Service
      - To
      - Lettings
      - Role
      - Tenancy
  /api/progression/lettings/setestimatedmoveindate:
    put:
      summary: Change the estimated move in date for the tenancy.
      description: Change the estimated move in date for the tenancy..
      operationId: LettingsProgression_SetEstimatedMoveInDateBydataContract
      x-api-path-slug: apiprogressionlettingssetestimatedmoveindate-put
      parameters:
      - in: body
        name: dataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Change
      - Estimated
      - Move
      - In
      - Datethe
      - Tenancy
  /api/tenancy/{id}/setagreement:
    post:
      summary: Set Agreement type for the tenancy.
      description: Set agreement type for the tenancy..
      operationId: Tenancy_SetAgreementByidByagreementDataContract
      x-api-path-slug: apitenancyidsetagreement-post
      parameters:
      - in: body
        name: agreementDataContract
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: Tenant Role Id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Set
      - Agreement
      - Typethe
      - Tenancy
  /api/tenancy/{id}/setparking:
    post:
      summary: Set parking details for the tenancy.
      description: Set parking details for the tenancy..
      operationId: Tenancy_SetParkingByidByparkingDataContract
      x-api-path-slug: apitenancyidsetparking-post
      parameters:
      - in: path
        name: id
        description: Tenant Role Id
      - in: body
        name: parkingDataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Set
      - Parking
      - Detailsthe
      - Tenancy
  /api/tenancy/{id}/detachdocument:
    put:
      summary: Detaches a document from a tenancy role
      description: Detaches a document from a tenancy role.
      operationId: Tenancy_DetachDocumentByidBydocumentId
      x-api-path-slug: apitenancyiddetachdocument-put
      parameters:
      - in: query
        name: documentId
        description: The id of the document to detach
      - in: path
        name: id
        description: The id of the role to detach the document from
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Detaches
      - Document
      - From
      - Tenancy
      - Role
  /api/tenancy/{id}/settenancytype:
    post:
      summary: Updated tenancy type
      description: Updated tenancy type.
      operationId: Tenancy_SetTenancyTypeByidBytenancyTypeName
      x-api-path-slug: apitenancyidsettenancytype-post
      parameters:
      - in: path
        name: id
        description: The id of the role
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: tenancyTypeName
        description: Tenancy Type name
      responses:
        200:
          description: OK
      tags:
      - D
      - Tenancy
      - Type
  /api/tenancy/{id}/generaterentdemand:
    post:
      summary: Create next rent demand for the tenancy
      description: Create next rent demand for the tenancy.
      operationId: Tenancy_GenerateRentDemandByidBydueDate
      x-api-path-slug: apitenancyidgeneraterentdemand-post
      parameters:
      - in: query
        name: dueDate
        description: (Optional) Due date if not provided calculated from next rent
          date
      - in: path
        name: id
        description: Tenant Role Id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Next
      - Rent
      - Demandthe
      - Tenancy
  /api/tenancy/{id}/setadditionalservice:
    post:
      summary: Create/Update additional service on tenancy
      description: Create/update additional service on tenancy.
      operationId: Tenancy_SetAdditionalServiceByidByserviceDataContract
      x-api-path-slug: apitenancyidsetadditionalservice-post
      parameters:
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: body
        name: serviceDataContract
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Additional
      - Service
      - "On"
      - Tenancy
  /api/tenancy/{id}/removeadditionalservice/{additionalServiceId}:
    post:
      summary: Remove additional service from tenancy
      description: Remove additional service from tenancy.
      operationId: Tenancy_DeleteAdditionalServiceByidByadditionalServiceId
      x-api-path-slug: apitenancyidremoveadditionalserviceadditionalserviceid-post
      parameters:
      - in: path
        name: additionalServiceId
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Additional
      - Service
      - From
      - Tenancy
  /api/tenantreferncing/case/{tenancyRoleId}:
    get:
      summary: Gets a tenancy referencing case based on the role id supplied
      description: Gets a tenancy referencing case based on the role id supplied.
      operationId: TenantReferencing_GetCaseBytenancyRoleId
      x-api-path-slug: apitenantreferncingcasetenancyroleid-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: tenancyRoleId
        description: The id of the tenancy role the case linked to
      responses:
        200:
          description: OK
      tags:
      - S
      - Tenancy
      - Referencing
      - Case
      - Based
      - "On"
      - Role
      - Id
      - Supplied
    post:
      summary: Creates a tenancy referencing case using the role id supplied
      description: Creates a tenancy referencing case using the role id supplied.
      operationId: TenantReferencing_CreateCaseBytenancyRoleId
      x-api-path-slug: apitenantreferncingcasetenancyroleid-post
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: tenancyRoleId
        description: The tenancy id the created case will be linked to
      responses:
        200:
          description: OK
      tags:
      - Creates
      - Tenancy
      - Referencing
      - Case
      - Using
      - Role
      - Id
      - Supplied
  /api/tenantreferncing/applications/{caseId}:
    get:
      summary: Gets all tenancy referencing applications for the caseId provided
      description: Gets all tenancy referencing applications for the caseid provided.
      operationId: TenantReferencing_GetApplicationsBycaseId
      x-api-path-slug: apitenantreferncingapplicationscaseid-get
      parameters:
      - in: path
        name: caseId
        description: The id of the case to get applications from
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - S
      - ""
      - Tenancy
      - Referencing
      - Applicationsthe
      - CaseId
      - Provided
  /api/tenantreferncing/addapplication/{caseId}/{tenancyRoleId}/{personId}/{productId}:
    post:
      summary: Creates a tenancy referencing application for a case using the details
        supplied
      description: Creates a tenancy referencing application for a case using the
        details supplied.
      operationId: TenantReferencing_CreateApplicationBycaseIdBytenancyRoleIdBypersonIdByproductId
      x-api-path-slug: apitenantreferncingaddapplicationcaseidtenancyroleidpersonidproductid-post
      parameters:
      - in: path
        name: caseId
        description: The id of the case to add the Application to
      - in: path
        name: personId
        description: The id of the individual the application is for
      - in: path
        name: productId
        description: The id of the product the client has chosen
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: tenancyRoleId
        description: The role id of the tenancy the case is linked to
      responses:
        200:
          description: OK
      tags:
      - Creates
      - Tenancy
      - Referencing
      - Applicationa
      - Case
      - Using
      - Details
      - Supplied
  /api/tenantreferncing/addguarantor/{caseId}/{tenancyRoleId}/{personId}:
    post:
      summary: Adds a Guarantor to a tenancy referencing application for a case using
        the details supplied
      description: Adds a guarantor to a tenancy referencing application for a case
        using the details supplied.
      operationId: TenantReferencing_CreateApplicationBycaseIdBytenancyRoleIdBypersonId
      x-api-path-slug: apitenantreferncingaddguarantorcaseidtenancyroleidpersonid-post
      parameters:
      - in: path
        name: caseId
        description: The id of the case to add the Guarantor to
      - in: path
        name: personId
        description: The id of the individual the application is for
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: tenancyRoleId
        description: The role id of the tenancy the case is linked to
      responses:
        200:
          description: OK
      tags:
      - S
      - Guarantor
      - To
      - Tenancy
      - Referencing
      - Applicationa
      - Case
      - Using
      - Details
      - Supplied
  /api/progression/lettings/setheadtenant:
    post:
      summary: Set the head tenant of a tenant role
      description: Set the head tenant of a tenant role.
      operationId: LettingsProgression_SetHeadTenantByidBytenantPersonIdBygroupId
      x-api-path-slug: apiprogressionlettingssetheadtenant-post
      parameters:
      - in: query
        name: groupId
        description: The id of the goup
      - in: query
        name: id
        description: The id of the tenant role
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: tenantPersonId
        description: The id of the person who should become head tenant
      responses:
        200:
          description: OK
      tags:
      - Set
      - Head
      - Tenant
      - Of
      - Tenant
      - Role
  /api/progression/lettings/signunsigndeed:
    put:
      summary: Set the head tenant of a tenant role
      description: Set the head tenant of a tenant role.
      operationId: LettingsProgression_SignUnsignDeedByguarantorIdBysigned
      x-api-path-slug: apiprogressionlettingssignunsigndeed-put
      parameters:
      - in: query
        name: guarantorId
        description: The guarantor id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: signed
        description: Sign true or false
      responses:
        200:
          description: OK
      tags:
      - Set
      - Head
      - Tenant
      - Of
      - Tenant
      - Role
  /api/progression/lettings/referencetenant:
    post:
      summary: Reference a tenant on a tenant role
      description: Reference a tenant on a tenant role.
      operationId: LettingsProgression_ReferenceTenantByidBytenantPersonIdByreferenceStatusByreferenceTypeBynameBynotes
      x-api-path-slug: apiprogressionlettingsreferencetenant-post
      parameters:
      - in: query
        name: id
        description: The id of the tenant role
      - in: query
        name: name
        description: The id of the person to reference
      - in: query
        name: notes
        description: Notes for the reference
      - in: query
        name: referenceDate
        description: Date of the reference if null today is used
      - in: query
        name: referenceStatus
        description: Whether the tenant has passed referencing or not
      - in: query
        name: referenceType
        description: Date of the reference if null today is used
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: tenantPersonId
        description: The id of the person to reference
      responses:
        200:
          description: OK
      tags:
      - Reference
      - Tenant
      - "On"
      - Tenant
      - Role
  /api/progression/lettings/referenceguarantor:
    post:
      summary: Reference a guarantor on a tenant role
      description: Reference a guarantor on a tenant role.
      operationId: LettingsProgression_ReferenceGuarantorByidByguarantorPersonIdByreferenceStatusBynameBynotesByreferen
      x-api-path-slug: apiprogressionlettingsreferenceguarantor-post
      parameters:
      - in: query
        name: guarantorPersonId
        description: The id of the person to reference
      - in: query
        name: id
        description: The id of the tenant role
      - in: query
        name: name
        description: The id of the tenant role
      - in: query
        name: notes
        description: Notes of reference
      - in: query
        name: referenceDate
        description: Date of the reference if null today is used
      - in: query
        name: referenceStatus
        description: Whether the guarantor has passed referencing or not
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Reference
      - Guarantor
      - "On"
      - Tenant
      - Role
  /api/progression/lettings/assignguarantortotenant:
    post:
      summary: Assign guarantor to a tenant and vice versa
      description: Assign guarantor to a tenant and vice versa.
      operationId: LettingsProgression_AssignGuarantorToTenantByidBydataContract
      x-api-path-slug: apiprogressionlettingsassignguarantortotenant-post
      parameters:
      - in: body
        name: dataContract
        description: The data contract
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: id
        description: The id of the tenant role
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Assign
      - Guarantor
      - To
      - Tenant
      - Vice
      - Versa
  /api/progression/lettings/uploadandattachtenantdocument:
    post:
      summary: Allows you to upload a document and attach it directly to a tenant.
      description: Allows you to upload a document and attach it directly to a tenant..
      operationId: LettingsProgression_UploadAndAttachTenantDocumentBytenantInfoIdBydocumentDetailsContract
      x-api-path-slug: apiprogressionlettingsuploadandattachtenantdocument-post
      parameters:
      - in: body
        name: documentDetailsContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: tenantInfoId
        description: The tenant Id
      responses:
        200:
          description: OK
      tags:
      - Allows
      - You
      - To
      - Upload
      - Document
      - Attach
      - It
      - Directly
      - To
      - Tenant
  /api/progression/lettings/uploadandattachlandlorddocument:
    post:
      summary: Allows you to upload a document and attach it directly to a tenant.
      description: Allows you to upload a document and attach it directly to a tenant..
      operationId: LettingsProgression_UploadAndAttachLandlordDocumentBylandlordInfoIdBydocumentDetailsContract
      x-api-path-slug: apiprogressionlettingsuploadandattachlandlorddocument-post
      parameters:
      - in: body
        name: documentDetailsContract
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: landlordInfoId
        description: The tenant Id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Allows
      - You
      - To
      - Upload
      - Document
      - Attach
      - It
      - Directly
      - To
      - Tenant
  /api/progression/lettings/{roleId}/inventory/uploaddocument:
    post:
      summary: Uploads an inventory document for a tenant role
      description: Uploads an inventory document for a tenant role.
      operationId: LettingsProgression_UploadAndAttachInventoryDocumentByroleIdBydocumentSaveCommand
      x-api-path-slug: apiprogressionlettingsroleidinventoryuploaddocument-post
      parameters:
      - in: body
        name: documentSaveCommand
        schema:
          $ref: '#/definitions/holder'
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
      - Uploads
      - Inventory
      - Documenta
      - Tenant
      - Role
  /api/progression/lettings/{roleId}/inventory/setrequired:
    post:
      summary: Sets whether inventory is needed on tenant role
      description: Sets whether inventory is needed on tenant role.
      operationId: LettingsProgression_SetInventoryRequiredByroleIdByrequired
      x-api-path-slug: apiprogressionlettingsroleidinventorysetrequired-post
      parameters:
      - in: query
        name: required
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: roleId
        description: Tenant Role Id
      responses:
        200:
          description: OK
      tags:
      - Sets
      - Whether
      - Inventory
      - Is
      - Needed
      - "On"
      - Tenant
      - Role
  /api/progression/lettings/{roleId}/inventory/savenote:
    post:
      summary: Add a note to a tenant role inventory
      description: Add a note to a tenant role inventory.
      operationId: LettingsProgression_SaveInventoryNoteByroleIdBynote
      x-api-path-slug: apiprogressionlettingsroleidinventorysavenote-post
      parameters:
      - in: query
        name: note
        description: Note text
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
      - Note
      - To
      - Tenant
      - Role
      - Inventory
  /api/progression/lettings/{roleId}/removetenantcharge:
    delete:
      summary: Remove charges from a tenant role
      description: Remove charges from a tenant role.
      operationId: LettingsProgression_RemoveTenantChargesByroleIdBychargeIds
      x-api-path-slug: apiprogressionlettingsroleidremovetenantcharge-delete
      parameters:
      - in: query
        name: chargeIds
        description: The ids of the charges to remove
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: roleId
        description: The tenant role id
      responses:
        200:
          description: OK
      tags:
      - Remove
      - Charges
      - From
      - Tenant
      - Role
  /api/progression/lettings/{roleId}/addpayment:
    post:
      summary: Add Tenant Payment
      description: Add tenant payment.
      operationId: LettingsProgression_AddTenantPaymentByroleIdByaddTenantPaymentDataContract
      x-api-path-slug: apiprogressionlettingsroleidaddpayment-post
      parameters:
      - in: body
        name: addTenantPaymentDataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: roleId
      responses:
        200:
          description: OK
      tags:
      - Tenant
      - Payment
  /api/progression/lettings/{id}/setdefaultmilestones:
    post:
      summary: Set tenant role milestones as the defaults for agency
      description: Set tenant role milestones as the defaults for agency.
      operationId: LettingsProgression_SetRoleMilestonesAsDefaultByid
      x-api-path-slug: apiprogressionlettingsidsetdefaultmilestones-post
      parameters:
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Set
      - Tenant
      - Role
      - Milestones
      - As
      - Defaultsagency
  /api/progression/lettings/{id}/resetmilestones:
    post:
      summary: Reset tenant role milestones back to agency defaults
      description: Reset tenant role milestones back to agency defaults.
      operationId: LettingsProgression_ResetRoleMilestonesToDefaultByid
      x-api-path-slug: apiprogressionlettingsidresetmilestones-post
      parameters:
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Reset
      - Tenant
      - Role
      - Milestones
      - Back
      - To
      - Agency
      - Defaults
  /api/property/{id}/tenantroles:
    get:
      summary: Get a list of all current and ended tenant roles from a property id.
      description: Get a list of all current and ended tenant roles from a property
        id..
      operationId: Property_TenantRolesByPropertyIdByid
      x-api-path-slug: apipropertyidtenantroles-get
      parameters:
      - in: path
        name: id
        description: The Id of the property
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - ""
      - Current
      - Ended
      - Tenant
      - Roles
      - From
      - Property
      - Id
  /api/tenancy/{id}/rentdemands:
    get:
      summary: Get rent demands for the tenant role
      description: Get rent demands for the tenant role.
      operationId: Tenancy_GetRentDemandsByidBystartDateByendDateByincludeForecastBypageSizeBypageNumber
      x-api-path-slug: apitenancyidrentdemands-get
      parameters:
      - in: query
        name: endDate
      - in: path
        name: id
      - in: query
        name: includeForecast
      - in: query
        name: pageNumber
      - in: query
        name: pageSize
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: startDate
      responses:
        200:
          description: OK
      tags:
      - Rent
      - Demandsthe
      - Tenant
      - Role
  /api/tenantreferncing/submitcase/{tenancyRoleId}/{caseId}:
    put:
      summary: Submits a tenant referencing case for processing
      description: Submits a tenant referencing case for processing.
      operationId: TenantReferencing_SubmitCaseForReferencingBytenancyRoleIdBycaseId
      x-api-path-slug: apitenantreferncingsubmitcasetenancyroleidcaseid-put
      parameters:
      - in: path
        name: caseId
        description: The id of the case to submit
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: tenancyRoleId
        description: The role id of the tenancy the case is linked to
      responses:
        200:
          description: OK
      tags:
      - Submits
      - Tenant
      - Referencing
      - Caseprocessing
  /api/progression/lettings/remarket:
    post:
      summary: Remarket a Letting. Completes the PropertyLettingRole and the TenantRole
        and creates a new PropertyLettingRole
      description: Remarket a letting. completes the propertylettingrole and the tenantrole
        and creates a new propertylettingrole.
      operationId: LettingsProgression_RemarketByremarketCommandDataContract
      x-api-path-slug: apiprogressionlettingsremarket-post
      parameters:
      - in: body
        name: remarketCommandDataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Remarket
      - Letting
      - ""
      - Completes
      - PropertyLettingRole
      - TenantRole
      - Creates
      - New
      - PropertyLettingRole
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