---
swagger: "2.0"
x-collection-name: TidyHQ
x-complete: 1
info:
  title: API Evangelist Analysis API
  description: this-is-an-api-that-provides-access-to-blog-posts-across-the-api-evangelist-network-
  termsOfService: http://developer.apievangelist.com/index.html
  contact:
    name: Kin Lane
    url: http://kinlane.com
    email: info@apievangelist.com
  license:
    name: MIT
    url: http://opensource.org/licenses/MIT
  version: "1.0"
host: api.apievangelist.com
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /analyses/d:
    get:
      summary: Pull analysis
      description: Returns a list of all blog posts filtered by keyword.
      operationId: getAnalysis
      x-api-path-slug: analysesd-get
      parameters:
      - in: query
        name: appid
        description: application id for application making calls
      - in: query
        name: appkey
        description: application key for application making calls
      - in: query
        name: query
        description: a text query to search across posts
      responses:
        200:
          description: Successful Image Manipulation
          schema:
            type: array
            items:
              $ref: '#/definitions/Image'
      tags:
      - Analysis
      - Blogs
  /analysis/{id}:
    get:
      summary: Retrieve a blog post using its ID
      description: Returns a blog post detail
      operationId: getAnalysis
      x-api-path-slug: analysisid-get
      parameters:
      - in: query
        name: appid
        description: application id for application making calls
      - in: query
        name: appkey
        description: application key for application making calls
      - in: path
        name: id
        description: id of the blog post to be returned
      responses:
        200:
          description: Successful Image Manipulation
          schema:
            type: array
            items:
              $ref: '#/definitions/Image'
      tags:
      - Analysis
      - Blogs
---