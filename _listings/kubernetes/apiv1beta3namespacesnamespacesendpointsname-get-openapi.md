---
swagger: "2.0"
x-collection-name: Kubernetes
x-complete: 0
info:
  title: Kubernetes Get Namespaces Endpoints Name
  version: 1.0.0
  description: Read the specified endpoints.
host: /api/v1beta3
basePath: 127.0.0.1:6443
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1beta3/endpoints:
    get:
      summary: Get Endpoints
      description: List objects of kind endpoints.
      operationId: listEndpoints
      x-api-path-slug: apiv1beta3endpoints-get
      responses:
        200:
          description: OK
      tags:
      - Endpoints
  /api/v1beta3/events:
    get:
      summary: Get Events
      description: List objects of kind event.
      operationId: listEvent
      x-api-path-slug: apiv1beta3events-get
      responses:
        200:
          description: OK
      tags:
      - Events
  /api/v1beta3/limitranges:
    get:
      summary: Get Limitranges
      description: List objects of kind limitrange.
      operationId: listLimitRange
      x-api-path-slug: apiv1beta3limitranges-get
      responses:
        200:
          description: OK
      tags:
      - Limitranges
  /api/v1beta3/namespaces:
    get:
      summary: Get Namespaces
      description: List objects of kind namespace.
      operationId: listNamespace
      x-api-path-slug: apiv1beta3namespaces-get
      responses:
        200:
          description: OK
      tags:
      - Namespaces
    post:
      summary: Post Namespaces
      description: Create a namespace.
      operationId: createNamespace
      x-api-path-slug: apiv1beta3namespaces-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Namespaces
  /api/v1beta3/namespaces/{namespaces}/bindings:
    post:
      summary: Post Namespaces Bindings
      description: Create a binding.
      operationId: createBinding
      x-api-path-slug: apiv1beta3namespacesnamespacesbindings-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Bindings
  /api/v1beta3/namespaces/{namespaces}/endpoints:
    get:
      summary: Get Namespaces Endpoints
      description: List objects of kind endpoints.
      operationId: listEndpoints
      x-api-path-slug: apiv1beta3namespacesnamespacesendpoints-get
      parameters:
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Endpoints
    post:
      summary: Post Namespaces Endpoints
      description: Create a endpoints.
      operationId: createEndpoints
      x-api-path-slug: apiv1beta3namespacesnamespacesendpoints-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Endpoints
  /api/v1beta3/namespaces/{namespaces}/endpoints/{name}:
    get:
      summary: Get Namespaces Endpoints Name
      description: Read the specified endpoints.
      operationId: readEndpoints
      x-api-path-slug: apiv1beta3namespacesnamespacesendpointsname-get
      parameters:
      - in: path
        name: name
        description: name of the Endpoints
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Endpoints
      - Name
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