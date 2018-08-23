---
swagger: "2.0"
x-collection-name: Shopify
x-complete: 1
info:
  title: Shopify API
  description: todo-add-description
  version: 1.0.0
host: DefaultParameterValue:DefaultParameterValue@DefaultParameterValue.myshopify.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /admin/blogs.json:
    get:
      summary: Get a list of all blogs
      description: Get a list of all blogs.
      operationId: getAdminBlogs.json
      x-api-path-slug: adminblogs-json-get
      parameters:
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - List
      - Blogs
  /admin/blogs/count.json:
    get:
      summary: Get a count of all blogs
      description: Get a count of all blogs.
      operationId: getAdminBlogsCount.json
      x-api-path-slug: adminblogscount-json-get
      parameters:
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - Commerce
      - Count
      - Blogs
---