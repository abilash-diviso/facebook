---
swagger: "2.0"
x-collection-name: Facebook
x-complete: 0
info:
  title: Facebook Get Search
  description: Search over all public objects in the social graph
  version: 1.0.0
host: graph.facebook.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /search:
    get:
      summary: Get Search
      description: Search over all public objects in the social graph
      operationId: getSearch
      x-api-path-slug: search-get
      parameters:
      - in: query
        name: q
        description: The search string
      - in: query
        name: type
        description: 'Supports these types of objects: All public posts (post), people
          (user), pages (page), events                                                        (event),
          groups (group), check-ins (checkin)'
      responses:
        200:
          description: OK
      tags:
      - Search
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