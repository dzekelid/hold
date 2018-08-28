---
swagger: "2.0"
x-collection-name: Box
x-complete: 0
info:
  title: Box Create New Legal Hold Policy
  description: Create a new Legal Hold Policy. Optional date filter may be passed.
    If Policy has a date filter, any Custodian assignments will apply only to file
    versions created or uploaded inside of the date range.
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