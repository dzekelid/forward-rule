---
swagger: "2.0"
x-collection-name: Google Compute Engine
x-complete: 0
info:
  title: Google Compute Engine API Get Forwarding Rule
  description: Returns the specified ForwardingRule resource. Get a list of available
    forwarding rules by making a list() request.
  contact:
    name: Google
    url: https://google.com
  version: v1
host: www.googleapis.com
basePath: /compute/v1/projects
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{project}/global/forwardingRules:
    get:
      summary: Get Forwarding Rules
      description: Retrieves a list of ForwardingRule resources available to the specified
        project.
      operationId: compute.globalForwardingRules.list
      x-api-path-slug: projectglobalforwardingrules-get
      parameters:
      - in: query
        name: filter
        description: Sets a filter expression for filtering listed resources, in the
          form filter={expression}
      - in: query
        name: maxResults
        description: The maximum number of results per page that should be returned
      - in: query
        name: orderBy
        description: Sorts list results by a certain order
      - in: query
        name: pageToken
        description: Specifies a page token to use
      - in: path
        name: project
        description: Project ID for this request
      responses:
        200:
          description: OK
      tags:
      - Forward Rule
    post:
      summary: Create Forwarding Rule
      description: Creates a ForwardingRule resource in the specified project and
        region using the data included in the request.
      operationId: compute.globalForwardingRules.insert
      x-api-path-slug: projectglobalforwardingrules-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: project
        description: Project ID for this request
      responses:
        200:
          description: OK
      tags:
      - Forward Rule
  /{project}/global/forwardingRules/{forwardingRule}:
    delete:
      summary: Delete Forwarding Rule
      description: Deletes the specified ForwardingRule resource.
      operationId: compute.globalForwardingRules.delete
      x-api-path-slug: projectglobalforwardingrulesforwardingrule-delete
      parameters:
      - in: path
        name: forwardingRule
        description: Name of the ForwardingRule resource to delete
      - in: path
        name: project
        description: Project ID for this request
      responses:
        200:
          description: OK
      tags:
      - Forward Rule
    get:
      summary: Get Forwarding Rule
      description: Returns the specified ForwardingRule resource. Get a list of available
        forwarding rules by making a list() request.
      operationId: compute.globalForwardingRules.get
      x-api-path-slug: projectglobalforwardingrulesforwardingrule-get
      parameters:
      - in: path
        name: forwardingRule
        description: Name of the ForwardingRule resource to return
      - in: path
        name: project
        description: Project ID for this request
      responses:
        200:
          description: OK
      tags:
      - Forward Rule
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