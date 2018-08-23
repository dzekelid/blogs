---
swagger: "2.0"
x-collection-name: Blogger
x-complete: 0
info:
  title: Blogger API Get User Blog
  description: Gets one blog and user info pair by blogId and userId.
  contact:
    name: Google
    url: https://google.com
  version: v3
host: www.googleapis.com
basePath: /blogger/v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /users/{userId}/blogs/{blogId}:
    get:
      summary: Get User Blog
      description: Gets one blog and user info pair by blogId and userId.
      operationId: blogger.blogUserInfos.get
      x-api-path-slug: usersuseridblogsblogid-get
      parameters:
      - in: path
        name: blogId
        description: The ID of the blog to get
      - in: query
        name: maxPosts
        description: Maximum number of posts to pull back with the blog
      - in: path
        name: userId
        description: ID of the user whose blogs are to be fetched
      responses:
        200:
          description: OK
      tags:
      - User Blogs
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