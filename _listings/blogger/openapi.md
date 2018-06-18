---
swagger: "2.0"
x-collection-name: Blogger
x-complete: 1
info:
  title: Blogger
  description: api-for-access-to-the-data-within-blogger-
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
---