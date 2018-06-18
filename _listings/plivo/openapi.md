---
swagger: "2.0"
x-collection-name: Plivo
x-complete: 1
info:
  title: Codenvy Account API
  description: this-is-the-api-for-managing-codenvy-account-
  version: 1.0.0
host: /account
basePath: https://codenvy.com/api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /blogs/:
    post:
      summary: Post Blogs
      description: Creates a new Story.
      operationId: creates-a-new-story
      x-api-path-slug: blogs-post
      parameters:
      - in: query
        name: body (required)
        description: Content of the blog post
      - in: query
        name: latitude
        description: Latitude for the blog post
      - in: query
        name: longitude
        description: Longitude for the blog post
      - in: query
        name: photo_ids
        description: Comma separated list of Photo ID values to post with the blog
      - in: query
        name: tags
        description: Comma separated list of tags
      - in: query
        name: title (required)
        description: Title for the blog post
      responses:
        200:
          description: OK
      tags:
      - Blogs
  /blogs/:id:
    put:
      summary: Put Blogs
      description: Updates the Story.
      operationId: updates-the-story
      x-api-path-slug: blogsid-put
      parameters:
      - in: query
        name: body
        description: Content of the blog post
      - in: query
        name: id (required)
        description: The Blog Post ID to update
      - in: query
        name: latitude
        description: Latitude for the blog post
      - in: query
        name: longitude
        description: Longitude for the blog post
      - in: query
        name: photo_ids
        description: Comma separated list of Photo IDs for photos that are in the
          blog post
      - in: query
        name: tags
        description: Comma separated list of tags
      - in: query
        name: title
        description: Title for the blog post
      responses:
        200:
          description: OK
      tags:
      - Blogs
      - :id
  /blogs/:id/comments:
    post:
      summary: Post Blogs Comments
      description: Creates a comment for the Story.
      operationId: creates-a-comment-for-the-story
      x-api-path-slug: blogsidcomments-post
      parameters:
      - in: query
        name: body (required)
        description: Content of the comment
      - in: query
        name: id (required)
        description: The Story ID to create a comment for
      responses:
        200:
          description: OK
      tags:
      - Blogs
      - :id
      - Comments
---