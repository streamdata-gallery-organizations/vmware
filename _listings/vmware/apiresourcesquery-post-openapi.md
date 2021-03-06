---
swagger: "2.0"
x-collection-name: VMWare
x-complete: 0
info:
  title: VMWare vRealize Operations Get Resources
  description: 'TODO: Add Description'
  version: 1.0.0
host: example.com
basePath: /suite-api/api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/auth/token/acquire:
    post:
      summary: RUN FIRST - Get vR Ops Auth Token
      description: 'TODO: Add Description'
      operationId: ApiAuthTokenAcquirePost
      x-api-path-slug: apiauthtokenacquire-post
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Auth
      - Token
      - Acquire
  /api/alerts/query:
    post:
      summary: Query Alerts
      description: 'TODO: Add Description'
      operationId: ApiAlertsQueryPost
      x-api-path-slug: apialertsquery-post
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Alerts
      - Query
  /api/alerts/7c2a4f9a-fd04-4300-b85c-cda555782e86:
    get:
      summary: Get Alert
      description: 'TODO: Add Description'
      operationId: ApiAlerts7c2a4f9aFd044300B85cCda555782e86Get
      x-api-path-slug: apialerts7c2a4f9afd044300b85ccda555782e86-get
      parameters:
      - in: header
        name: Accept
      responses:
        200:
          description: OK
      tags:
      - Alerts
  /api/alertdefinitions/{alertDefinitionId}:
    get:
      summary: Get Alert Definition
      description: 'TODO: Add Description'
      operationId: ApiAlertdefinitionsByAlertDefinitionIdGet
      x-api-path-slug: apialertdefinitionsalertdefinitionid-get
      parameters:
      - in: header
        name: Accept
      - in: path
        name: alertDefinitionId
      responses:
        200:
          description: OK
      tags:
      - Alertdefinitions
      - AlertDefinitionId
  /symptoms:
    get:
      summary: Get Impacted Resource Symptoms
      description: 'TODO: Add Description'
      operationId: SymptomsGet
      x-api-path-slug: symptoms-get
      parameters:
      - in: header
        name: Accept
      - in: query
        name: resourceId
      responses:
        200:
          description: OK
      tags:
      - Symptoms
  /alerts/contributingsymptoms:
    get:
      summary: Get Alert Contributing Symptoms
      description: Added in vROps 6.7
      operationId: AlertsContributingsymptomsGet
      x-api-path-slug: alertscontributingsymptoms-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: query
        name: id
      responses:
        200:
          description: OK
      tags:
      - Alerts
      - Contributingsymptoms
  /resources:
    get:
      summary: Get Resources by Query and Save to var
      description: |-
        Test script will extract resource IDs from the response and load into the env as "resourceIds"
        You can then use this within the body of a request
      operationId: ResourcesGet5
      x-api-path-slug: resources-get
      parameters:
      - in: header
        name: Accept
      - in: query
        name: resourceKind
      responses:
        200:
          description: OK
      tags:
      - Resources
  /internal/agent/upgrade:
    post:
      summary: Update EP Ops Agent
      description: 'TODO: Add Description'
      operationId: InternalAgentUpgradePost
      x-api-path-slug: internalagentupgrade-post
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: header
        name: X-vRealizeOps-API-use-unsupported
      responses:
        200:
          description: OK
      tags:
      - Internal
      - Agent
      - Upgrade
  /adapterkinds/EP Ops Adapter/resourcekinds/EP Ops Agent/resources:
    get:
      summary: Get Agent Status on Upgrade
      description: Need agent ID (token)
      operationId: AdapterkindsEPOpsAdapterResourcekindsEPOpsAgentResourcesGet
      x-api-path-slug: adapterkindsep-ops-adapterresourcekindsep-ops-agentresources-get
      parameters:
      - in: header
        name: Accept
      - in: query
        name: identifiers[agentID]
      responses:
        200:
          description: OK
      tags:
      - Adapterkinds
      - EP
      - Ops
      - Adapter
      - Resourcekinds
      - EP
      - Ops
      - Agent
      - Resources
  /api/resources/{agentResourceId}/relationships:
    get:
      summary: Get OS Resource ID and Save
      description: 'TODO: Add Description'
      operationId: ApiResourcesRelationshipsByAgentResourceIdGet
      x-api-path-slug: apiresourcesagentresourceidrelationships-get
      parameters:
      - in: header
        name: Accept
      - in: path
        name: agentResourceId
      responses:
        200:
          description: OK
      tags:
      - Resources
      - AgentResourceId
      - Relationships
  /api/resources/adapters/{adapterInstanceId}:
    post:
      summary: Create an EPOPS Unix MultiProcess Monitor Resource
      description: 'TODO: Add Description'
      operationId: ApiResourcesAdaptersByAdapterInstanceIdPost3
      x-api-path-slug: apiresourcesadaptersadapterinstanceid-post
      parameters:
      - in: header
        name: Accept
      - in: path
        name: adapterInstanceId
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Resources
      - Adapters
      - AdapterInstanceId
  /api/resources/{osResourceId}/relationships/children:
    post:
      summary: Add Child Resource to a Resource
      description: "This operation adds a child resource to a resource.  \n\nAPI documentation
        states that POST is additive while PUT is destructive (i.e. overwites existing
        relationships).\n\nJSON body includes an array of child objects to add.  \n\nThe
        call does not provide a lot of detail for failure, but it seems\nthat if you
        have an invalid UUID for a child or the child is already related\nthen it
        will fail with 400.\n\n204 is a successful call."
      operationId: ApiResourcesRelationshipsChildrenByOsResourceIdPost
      x-api-path-slug: apiresourcesosresourceidrelationshipschildren-post
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: osResourceId
      responses:
        200:
          description: OK
      tags:
      - Resources
      - OsResourceId
      - Relationships
      - Children
  /api/resources/{epopsMonitorResourceId}/monitoringstate/start:
    put:
      summary: Start Monitoring a Resource
      description: 'TODO: Add Description'
      operationId: ApiResourcesMonitoringstateStartByEpopsMonitorResourceIdPut
      x-api-path-slug: apiresourcesepopsmonitorresourceidmonitoringstatestart-put
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: path
        name: epopsMonitorResourceId
      responses:
        200:
          description: OK
      tags:
      - Resources
      - EpopsMonitorResourceId
      - Monitoringstate
      - Start
  /internal/resources/groups:
    get:
      summary: Get Custom Groups
      description: 'TODO: Add Description'
      operationId: InternalResourcesGroupsGet
      x-api-path-slug: internalresourcesgroups-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: X-vRealizeOps-API-use-unsupported
      responses:
        200:
          description: OK
      tags:
      - Internal
      - Resources
      - Groups
    post:
      summary: Create Custom Group
      description: 'TODO: Add Description'
      operationId: InternalResourcesGroupsPost
      x-api-path-slug: internalresourcesgroups-post
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: header
        name: X-vRealizeOps-API-use-unsupported
      responses:
        200:
          description: OK
      tags:
      - Internal
      - Resources
      - Groups
  /api/reportdefinitions:
    get:
      summary: Get Report Definitions
      description: Gets all - to get a single report ID, just add /<report def id>
      operationId: ApiReportdefinitionsGet
      x-api-path-slug: apireportdefinitions-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Reportdefinitions
  /api/reports:
    get:
      summary: Get Generated Reports
      description: |-
        You can check status of report runs this way.
        To get a specific generated report add /<report id>
      operationId: ApiReportsGet
      x-api-path-slug: apireports-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Reports
    post:
      summary: Generate a report
      description: |-
        You will need to update several items in the body such as:
          - ID of resource you wish to run this report on
          - ID of the report you wish to run
          - Traversal Spec for the report (you can get this from the API query
        "Get Report Definitions", the travesal spec must match the resource type.
      operationId: ApiReportsPost
      x-api-path-slug: apireports-post
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Reports
  /reports/be9097f7-0c8c-4a33-a855-faafb6f03a1d/download:
    get:
      summary: Download Report
      description: 'TODO: Add Description'
      operationId: ReportsBe9097f70c8c4a33A855Faafb6f03a1dDownloadGet
      x-api-path-slug: reportsbe9097f70c8c4a33a855faafb6f03a1ddownload-get
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      - in: query
        name: format
      responses:
        200:
          description: OK
      tags:
      - Reports
      - ""
      - Download
  /api/adapterkinds:
    get:
      summary: Get Adapter Types (Kinds)
      description: 'TODO: Add Description'
      operationId: ApiAdapterkindsGet
      x-api-path-slug: apiadapterkinds-get
      parameters:
      - in: header
        name: Accept
      responses:
        200:
          description: OK
      tags:
      - Adapterkinds
  /api/adapters:
    get:
      summary: Get Adapter Instances
      description: 'TODO: Add Description'
      operationId: ApiAdaptersGet
      x-api-path-slug: apiadapters-get
      parameters:
      - in: header
        name: Accept
      responses:
        200:
          description: OK
      tags:
      - Adapters
    post:
      summary: Create a Python Adapter Instance
      description: "Be sure to check values in the JSON body for credentials.\nAlso
        note you will need to start the adapter using \"Star an adapter instance\"
        \nafter creation using the UUID from the response.\n\nIf you aren't using
        a CA, the certificate will have to be added via the UI\nI do not know of a
        way to do this via the REST API"
      operationId: ApiAdaptersPost2
      x-api-path-slug: apiadapters-post
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Adapters
  /adapters:
    get:
      summary: Get An Adapter Instance(s) of Type (Kind)
      description: 'TODO: Add Description'
      operationId: AdaptersGet
      x-api-path-slug: adapters-get
      parameters:
      - in: header
        name: Accept
      - in: query
        name: adapterKindKey
      responses:
        200:
          description: OK
      tags:
      - Adapters
  /api/adapters/617d20fd-536a-4bea-9f5e-4c01dd845ddc/monitoringstate/start:
    put:
      summary: Start an adapter instance
      description: |-
        Replace the UUID with the ID of the adapter instance you want to start
        This can be retrieved using Get Adapter Instances
      operationId: ApiAdapters617d20fd536a4bea9f5e4c01dd845ddcMonitoringstateStartPut
      x-api-path-slug: apiadapters617d20fd536a4bea9f5e4c01dd845ddcmonitoringstatestart-put
      parameters:
      - in: header
        name: Accept
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Adapters
      - Start
  /api/resources/query:
    post:
      summary: Get Resources
      description: 'TODO: Add Description'
      operationId: ApiResourcesQueryPost
      x-api-path-slug: apiresourcesquery-post
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Resources
      - Query
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