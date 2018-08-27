---
swagger: "2.0"
x-collection-name: Blogger
x-complete: 0
info:
  title: Blogger API Add Blog Post
  description: Add a post.
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
  /blogs/{blogId}/posts:
    get:
      summary: Get Blog Posts
      description: Retrieves a list of posts, possibly filtered.
      operationId: blogger.posts.list
      x-api-path-slug: blogsblogidposts-get
      parameters:
      - in: path
        name: blogId
        description: ID of the blog to fetch posts from
      - in: query
        name: endDate
        description: Latest post date to fetch, a date-time with RFC 3339 formatting
      - in: query
        name: fetchBodies
        description: 'Whether the body content of posts is included (default: true)'
      - in: query
        name: fetchImages
        description: Whether image URL metadata for each post is included
      - in: query
        name: labels
        description: Comma-separated list of labels to search for
      - in: query
        name: maxResults
        description: Maximum number of posts to fetch
      - in: query
        name: orderBy
        description: Sort search results
      - in: query
        name: pageToken
        description: Continuation token if the request is paged
      - in: query
        name: startDate
        description: Earliest post date to fetch, a date-time with RFC 3339 formatting
      - in: query
        name: status
        description: Statuses to include in the results
      - in: query
        name: view
        description: Access level with which to view the returned result
      responses:
        200:
          description: OK
      tags:
      - Blog Post
    post:
      summary: Add Blog Post
      description: Add a post.
      operationId: blogger.posts.insert
      x-api-path-slug: blogsblogidposts-post
      parameters:
      - in: path
        name: blogId
        description: ID of the blog to add the post to
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: fetchBody
        description: 'Whether the body content of the post is included with the result
          (default: true)'
      - in: query
        name: fetchImages
        description: 'Whether image URL metadata for each post is included in the
          returned result (default: false)'
      - in: query
        name: isDraft
        description: 'Whether to create the post as a draft (default: false)'
      responses:
        200:
          description: OK
      tags:
      - Blog Post
  /blogs/{blogId}/posts/bypath:
    get:
      summary: Get Blog Post by Path
      description: Retrieve a Post by Path.
      operationId: blogger.posts.getByPath
      x-api-path-slug: blogsblogidpostsbypath-get
      parameters:
      - in: path
        name: blogId
        description: ID of the blog to fetch the post from
      - in: query
        name: maxComments
        description: Maximum number of comments to pull back on a post
      - in: query
        name: path
        description: Path of the Post to retrieve
      - in: query
        name: view
        description: Access level with which to view the returned result
      responses:
        200:
          description: OK
      tags:
      - Blog Post
  /blogs/{blogId}/posts/{postId}:
    delete:
      summary: Delete Blog Post
      description: Delete a post by ID.
      operationId: blogger.posts.delete
      x-api-path-slug: blogsblogidpostspostid-delete
      parameters:
      - in: path
        name: blogId
        description: The ID of the Blog
      - in: path
        name: postId
        description: The ID of the Post
      responses:
        200:
          description: OK
      tags:
      - Blog Post
    get:
      summary: Get Blog Post
      description: Get a post by ID.
      operationId: blogger.posts.get
      x-api-path-slug: blogsblogidpostspostid-get
      parameters:
      - in: path
        name: blogId
        description: ID of the blog to fetch the post from
      - in: query
        name: fetchBody
        description: 'Whether the body content of the post is included (default: true)'
      - in: query
        name: fetchImages
        description: 'Whether image URL metadata for each post is included (default:
          false)'
      - in: query
        name: maxComments
        description: Maximum number of comments to pull back on a post
      - in: path
        name: postId
        description: The ID of the post
      - in: query
        name: view
        description: Access level with which to view the returned result
      responses:
        200:
          description: OK
      tags:
      - Blog Post
    patch:
      summary: Update Blog Post
      description: Update a post. This method supports patch semantics.
      operationId: blogger.posts.patch
      x-api-path-slug: blogsblogidpostspostid-patch
      parameters:
      - in: path
        name: blogId
        description: The ID of the Blog
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: fetchBody
        description: 'Whether the body content of the post is included with the result
          (default: true)'
      - in: query
        name: fetchImages
        description: 'Whether image URL metadata for each post is included in the
          returned result (default: false)'
      - in: query
        name: maxComments
        description: Maximum number of comments to retrieve with the returned post
      - in: path
        name: postId
        description: The ID of the Post
      - in: query
        name: publish
        description: 'Whether a publish action should be performed when the post is
          updated (default: false)'
      - in: query
        name: revert
        description: 'Whether a revert action should be performed when the post is
          updated (default: false)'
      responses:
        200:
          description: OK
      tags:
      - Blog Post
    put:
      summary: Update Blog Post
      description: Update a post.
      operationId: blogger.posts.update
      x-api-path-slug: blogsblogidpostspostid-put
      parameters:
      - in: path
        name: blogId
        description: The ID of the Blog
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: fetchBody
        description: 'Whether the body content of the post is included with the result
          (default: true)'
      - in: query
        name: fetchImages
        description: 'Whether image URL metadata for each post is included in the
          returned result (default: false)'
      - in: query
        name: maxComments
        description: Maximum number of comments to retrieve with the returned post
      - in: path
        name: postId
        description: The ID of the Post
      - in: query
        name: publish
        description: 'Whether a publish action should be performed when the post is
          updated (default: false)'
      - in: query
        name: revert
        description: 'Whether a revert action should be performed when the post is
          updated (default: false)'
      responses:
        200:
          description: OK
      tags:
      - Blog Post
  /blogs/{blogId}/posts/{postId}/publish:
    post:
      summary: Publish Blog Post
      description: Publishes a draft post, optionally at the specific time of the
        given publishDate parameter.
      operationId: blogger.posts.publish
      x-api-path-slug: blogsblogidpostspostidpublish-post
      parameters:
      - in: path
        name: blogId
        description: The ID of the Blog
      - in: path
        name: postId
        description: The ID of the Post
      - in: query
        name: publishDate
        description: Optional date and time to schedule the publishing of the Blog
      responses:
        200:
          description: OK
      tags:
      - Blog Post
  /blogs/{blogId}/posts/{postId}/revert:
    post:
      summary: Revert Blog Post
      description: Revert a published or scheduled post to draft state.
      operationId: blogger.posts.revert
      x-api-path-slug: blogsblogidpostspostidrevert-post
      parameters:
      - in: path
        name: blogId
        description: The ID of the Blog
      - in: path
        name: postId
        description: The ID of the Post
      responses:
        200:
          description: OK
      tags:
      - Blog Post
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