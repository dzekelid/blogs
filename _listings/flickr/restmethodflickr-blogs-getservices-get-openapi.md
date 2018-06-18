---
swagger: "2.0"
x-collection-name: Flickr
x-complete: 0
info:
  title: Flickr Blogs Get Services
  description: Returns a list of Flickr supported blogging services.
  version: 1.0.0
host: api.flickr.com
basePath: /services/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/?method=flickr.blogs.getList:
    get:
      summary: Blogs Get List
      description: Get a list of configured blogs for the calling user.
      operationId: getRestMethodFlickr.blogs.getlist
      x-api-path-slug: restmethodflickr-blogs-getlist-get
      parameters:
      - in: query
        name: api_key
        description: Your API application key
      - in: query
        name: format
        description: Response format
      - in: query
        name: service
        description: Optionally only return blogs for a given service id
      responses:
        200:
          description: OK
      tags:
      - Blogs
      - GetList
  /rest/?method=flickr.blogs.getServices:
    get:
      summary: Blogs Get Services
      description: Returns a list of Flickr supported blogging services.
      operationId: getRestMethodFlickr.blogs.getservices
      x-api-path-slug: restmethodflickr-blogs-getservices-get
      parameters:
      - in: query
        name: api_key
        description: Your API application key
      - in: query
        name: format
        description: Response format
      responses:
        200:
          description: OK
      tags:
      - Blogs
      - GetServices
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