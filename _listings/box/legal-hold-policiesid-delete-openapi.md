---
swagger: "2.0"
x-collection-name: Box
x-complete: 0
info:
  title: Box Delete Legal Hold Policy
  description: Sends request to delete an existing Legal Hold Policy. Note that this
    is an asynchronous process - the Policy will not be fully deleted yet when the
    response comes back.
  version: 1.0.0
host: api.box.com
basePath: /2.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /legal_hold_policies:
    post:
      summary: Create New Legal Hold Policy
      description: Create a new Legal Hold Policy. Optional date filter may be passed.
        If Policy has a date filter, any Custodian assignments will apply only to
        file versions created or uploaded inside of the date range.
      operationId: createLegalHoldPolicy
      x-api-path-slug: legal-hold-policies-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Legal
      - Hold
      - Policies
    get:
      summary: Get Legal Hold Policies
      description: Get a list of Legal Hold Policies that belong to your Enterprise.
      operationId: getLegalHoldPolicies
      x-api-path-slug: legal-hold-policies-get
      parameters:
      - in: query
        name: limit
        description: Limit result size to this number
      - in: query
        name: marker
        description: Take from next_marker column of a prior call to get the next
          page
      - in: query
        name: policy_name
        description: Case insensitive prefix-match filter on Policy name
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Legal
      - Hold
      - Policies
  /legal_hold_policies/{ID}:
    put:
      summary: Update Existing Legal Hold Policy
      description: Update existing Legal Hold Policy. Only name and description can
        be modified.
      operationId: updateLegalHoldPolicy
      x-api-path-slug: legal-hold-policiesid-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: ID
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Legal
      - Hold
      - Policies
    get:
      summary: Get Legal Hold Policy
      description: Get details of a single Legal Hold Policy
      operationId: getLegalHoldPolicy
      x-api-path-slug: legal-hold-policiesid-get
      parameters:
      - in: path
        name: ID
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Legal
      - Hold
      - Policies
    delete:
      summary: Delete Legal Hold Policy
      description: Sends request to delete an existing Legal Hold Policy. Note that
        this is an asynchronous process - the Policy will not be fully deleted yet
        when the response comes back.
      operationId: deleteLegalHoldPolicy
      x-api-path-slug: legal-hold-policiesid-delete
      parameters:
      - in: path
        name: ID
      responses:
        200:
          description: OK
      tags:
      - Documents
      - Legal
      - Hold
      - Policies
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