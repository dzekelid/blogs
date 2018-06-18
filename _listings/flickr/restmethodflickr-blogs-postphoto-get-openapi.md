---
swagger: "2.0"
x-collection-name: Flickr
x-complete: 0
info:
  title: Flickr Blogs Add Photo
  description: Posts a photo to a blog.
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
  /rest/?method=flickr.blogs.postPhoto:
    get:
      summary: Blogs Add Photo
      description: Posts a photo to a blog.
      operationId: getRestMethodFlickr.blogs.addphoto
      x-api-path-slug: restmethodflickr-blogs-postphoto-get
      parameters:
      - in: query
        name: api_key
        description: Your API application key
      - in: query
        name: blog_id
        description: The ID of the blog to post to
      - in: query
        name: blog_password
        description: The password for the blog (used when the blog does not have a
          stored password)
      - in: query
        name: description
        description: The blog post body
      - in: query
        name: format
        description: Response format
      - in: query
        name: photo_id
        description: The ID of the photo to blog
      - in: query
        name: service
        description: A Flickr supported blogging service
      - in: query
        name: title
        description: The blog post title
      responses:
        200:
          description: OK
      tags:
      - Blogs
      - PostPhoto
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