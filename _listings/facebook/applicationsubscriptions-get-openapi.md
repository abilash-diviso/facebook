---
swagger: "2.0"
x-collection-name: Facebook
x-complete: 0
info:
  title: Facebook Get Application Subscriptions
  description: All of the subscriptions this application has for real-time notifications.
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
  /{album}:
    get:
      summary: Get Album
      description: A photo album
      operationId: getAlbum
      x-api-path-slug: album-get
      parameters:
      - in: path
        name: album
        description: Represents the ID of the album object
      responses:
        200:
          description: OK
      tags:
      - Album
  /{album}/photos:
    get:
      summary: Get Album Photos
      description: The photos contained in this album
      operationId: getAlbumPhotos
      x-api-path-slug: albumphotos-get
      parameters:
      - in: path
        name: album
        description: Represents the ID of the album object
      responses:
        200:
          description: OK
      tags:
      - Album
      - Photos
    post:
      summary: Post Album Photos
      description: Adds a photo to the album
      operationId: postAlbumPhotos
      x-api-path-slug: albumphotos-post
      parameters:
      - in: path
        name: album
        description: Represents the ID of the album object
      - in: query
        name: message
        description: Photo description
      responses:
        200:
          description: OK
      tags:
      - Album
      - Photos
  /{album}/likes:
    get:
      summary: Get Album Likes
      description: The likes made on this album
      operationId: getAlbumLikes
      x-api-path-slug: albumlikes-get
      parameters:
      - in: path
        name: album
        description: Represents the ID of the album object
      responses:
        200:
          description: OK
      tags:
      - Album
      - Likes
    post:
      summary: Post Album Likes
      description: Likes the album
      operationId: postAlbumLikes
      x-api-path-slug: albumlikes-post
      parameters:
      - in: path
        name: album
        description: Represents the ID of the album object
      responses:
        200:
          description: OK
      tags:
      - Album
      - Likes
    delete:
      summary: Delete Album Likes
      description: Unlikes the album
      operationId: deleteAlbumLikes
      x-api-path-slug: albumlikes-delete
      parameters:
      - in: path
        name: album
        description: Represents the ID of the album object
      responses:
        200:
          description: OK
      tags:
      - Album
      - Likes
  /{album}/comments:
    get:
      summary: Get Album Comments
      description: The comments made on this album
      operationId: getAlbumComments
      x-api-path-slug: albumcomments-get
      parameters:
      - in: path
        name: album
        description: Represents the ID of the album object
      responses:
        200:
          description: OK
      tags:
      - Album
      - Comments
    post:
      summary: Post Album Comments
      description: Posts a comment on the album
      operationId: postAlbumComments
      x-api-path-slug: albumcomments-post
      parameters:
      - in: path
        name: album
        description: Represents the ID of the album object
      - in: query
        name: message
        description: Comment text
      responses:
        200:
          description: OK
      tags:
      - Album
      - Comments
  /{album}/picture:
    get:
      summary: Get Album Picture
      description: The album's cover photo; the first picture uploaded to an album
        becomes the cover photo for the album.
      operationId: getAlbumPicture
      x-api-path-slug: albumpicture-get
      parameters:
      - in: path
        name: album
        description: Represents the ID of the album object
      - in: query
        name: type
        description: One of square (50x50), small (50 pixels wide, variable height),
          and large (about 200 pixels wide,                                                        variable
          height)
      responses:
        200:
          description: OK
      tags:
      - Album
      - Picture
  /{application}:
    get:
      summary: Get Application
      description: An application's profile
      operationId: getApplication
      x-api-path-slug: application-get
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      responses:
        200:
          description: OK
      tags:
      - Application
  /{application}/accounts:
    get:
      summary: Get Application Accounts
      description: Test User accounts associated with the application.
      operationId: getApplicationAccounts
      x-api-path-slug: applicationaccounts-get
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      responses:
        200:
          description: OK
      tags:
      - Application
      - Accounts
  /{application}/accounts/test-users:
    post:
      summary: Post Application Accounts Test Users
      description: Creates a test account for the application
      operationId: postApplicationAccountsTestUsers
      x-api-path-slug: applicationaccountstestusers-post
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      - in: query
        name: installed
        description: Install app for the test user upon creation
      - in: query
        name: name
        description: A name for the test user
      - in: query
        name: permissions
        description: List of extended permissions app granted for the new test user
          if installed is true
      responses:
        200:
          description: OK
      tags:
      - Application
      - Accounts
      - Test
      - Users
  /{application}/albums:
    get:
      summary: Get Application Albums
      description: The photo albums this application has created.
      operationId: getApplicationAlbums
      x-api-path-slug: applicationalbums-get
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      responses:
        200:
          description: OK
      tags:
      - Application
      - Albums
  /{application}/feed:
    get:
      summary: Get Application Feed
      description: The application's wall.
      operationId: getApplicationFeed
      x-api-path-slug: applicationfeed-get
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      responses:
        200:
          description: OK
      tags:
      - Application
      - Feed
    post:
      summary: Post Application Feed
      description: Posts a status message on the application's profile page
      operationId: postApplicationFeed
      x-api-path-slug: applicationfeed-post
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      - in: query
        name: message
        description: Status Message content
      responses:
        200:
          description: OK
      tags:
      - Application
      - Feed
  /{application}/insights:
    get:
      summary: Get Application Insights
      description: Usage metrics for this application
      operationId: getApplicationInsights
      x-api-path-slug: applicationinsights-get
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      responses:
        200:
          description: OK
      tags:
      - Application
      - Insights
  /{application}/links:
    get:
      summary: Get Application Links
      description: The application's posted links.
      operationId: getApplicationLinks
      x-api-path-slug: applicationlinks-get
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      responses:
        200:
          description: OK
      tags:
      - Application
      - Links
    post:
      summary: Post Application Links
      description: Posts a link on the application's profile page
      operationId: postApplicationLinks
      x-api-path-slug: applicationlinks-post
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      - in: query
        name: link
        description: Link URL
      - in: query
        name: message
        description: Link message
      responses:
        200:
          description: OK
      tags:
      - Application
      - Links
  /{application}/picture:
    get:
      summary: Get Application Picture
      description: The application's logo
      operationId: getApplicationPicture
      x-api-path-slug: applicationpicture-get
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      - in: query
        name: type
        description: One of square (50x50), small (50 pixels wide, variable height),
          and large (about 200 pixels wide,                                                        variable
          height)
      responses:
        200:
          description: OK
      tags:
      - Application
      - Picture
  /{application}/posts:
    get:
      summary: Get Application Adds
      description: The application's own posts.
      operationId: getApplicationAdds
      x-api-path-slug: applicationposts-get
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      responses:
        200:
          description: OK
      tags:
      - Application
      - Posts
  /{application}/reviews:
    get:
      summary: Get Application Reviews
      description: Reviews of this application
      operationId: getApplicationReviews
      x-api-path-slug: applicationreviews-get
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      responses:
        200:
          description: OK
      tags:
      - Application
      - Reviews
  /{application}/staticresources:
    get:
      summary: Get Application Staticresources
      description: Usage stats about the canvas application's static resources, such
        as javascript and CSS, and which ones are being flushed to browsers early.
      operationId: getApplicationStaticresources
      x-api-path-slug: applicationstaticresources-get
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      responses:
        200:
          description: OK
      tags:
      - Application
      - Staticresources
  /{application}/statuses:
    get:
      summary: Get Application Statuses
      description: The application's status updates
      operationId: getApplicationStatuses
      x-api-path-slug: applicationstatuses-get
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      responses:
        200:
          description: OK
      tags:
      - Application
      - Statuses
    post:
      summary: Post Application Statuses
      description: Posts a status message on the application's profile page
      operationId: postApplicationStatuses
      x-api-path-slug: applicationstatuses-post
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      - in: query
        name: message
        description: Status Message content
      responses:
        200:
          description: OK
      tags:
      - Application
      - Statuses
  /{application}/subscriptions:
    get:
      summary: Get Application Subscriptions
      description: All of the subscriptions this application has for real-time notifications.
      operationId: getApplicationSubscriptions
      x-api-path-slug: applicationsubscriptions-get
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      responses:
        200:
          description: OK
      tags:
      - Application
      - Subscriptions
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