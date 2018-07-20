---
swagger: "2.0"
x-collection-name: Facebook
x-complete: 0
info:
  title: Facebook Post Note Comments
  description: Posts a comment to this note.
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
    post:
      summary: Post Application Subscriptions
      description: Adds a real-time notification subscription for this application.
      operationId: postApplicationSubscriptions
      x-api-path-slug: applicationsubscriptions-post
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      - in: query
        name: callback_url
        description: A callback URL to which Facebook will post subscription updates
      - in: query
        name: fields
        description: List of properties for the `object` to monitor
      - in: query
        name: object
        description: Object to monitor - `user`, `permissions`, or `page`
      - in: query
        name: verify_token
        description: Token sent in the verification request
      responses:
        200:
          description: OK
      tags:
      - Application
      - Subscriptions
    delete:
      summary: Delete Application Subscriptions
      description: Deletes a real-time notification subscription for this application.
      operationId: deleteApplicationSubscriptions
      x-api-path-slug: applicationsubscriptions-delete
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      - in: query
        name: object
        description: Object to monitor - `user`, `permissions`, or `page`
      responses:
        200:
          description: OK
      tags:
      - Application
      - Subscriptions
  /{application}/tagged:
    get:
      summary: Get Application Tagged
      description: The photos, videos, and posts in which this application has been
        tagged.
      operationId: getApplicationTagged
      x-api-path-slug: applicationtagged-get
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      responses:
        200:
          description: OK
      tags:
      - Application
      - Tagged
  /{application}/translations:
    get:
      summary: Get Application Translations
      description: The translated strings for this application.
      operationId: getApplicationTranslations
      x-api-path-slug: applicationtranslations-get
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      responses:
        200:
          description: OK
      tags:
      - Application
      - Translations
    post:
      summary: Post Application Translations
      description: Uploads translated strings for this application.
      operationId: postApplicationTranslations
      x-api-path-slug: applicationtranslations-post
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      - in: query
        name: native_strings
        description: A JSON-encoded array of strings to translate
      responses:
        200:
          description: OK
      tags:
      - Application
      - Translations
    delete:
      summary: Delete Application Translations
      description: Deletes a translation string for this application.
      operationId: deleteApplicationTranslations
      x-api-path-slug: applicationtranslations-delete
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      - in: query
        name: native_hashes
        description: An array of native hashes
      responses:
        200:
          description: OK
      tags:
      - Application
      - Translations
  /{application}/scores:
    get:
      summary: Get Application Scores
      description: Scores for the user and their friends.
      operationId: getApplicationScores
      x-api-path-slug: applicationscores-get
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      responses:
        200:
          description: OK
      tags:
      - Application
      - Scores
    delete:
      summary: Delete Application Scores
      description: Deletes all the scores for the application.
      operationId: deleteApplicationScores
      x-api-path-slug: applicationscores-delete
      parameters:
      - in: path
        name: application
        description: Represents the ID of the application object
      responses:
        200:
          description: OK
      tags:
      - Application
      - Scores
  /{application}/achievements:
    post:
      summary: Post Application Achievements
      description: Registers an achievement for the application
      operationId: postApplicationAchievements
      x-api-path-slug: applicationachievements-post
      parameters:
      - in: query
        name: achievement
        description: Unique URL to the achievement
      - in: path
        name: application
        description: Represents the ID of the application object
      - in: query
        name: display_order
        description: Order of this achievement as it shows up in the achievement stories
          UI (low to high)
      responses:
        200:
          description: OK
      tags:
      - Application
      - Achievements
    delete:
      summary: Delete Application Achievements
      description: Unregisters an achievement for the application
      operationId: deleteApplicationAchievements
      x-api-path-slug: applicationachievements-delete
      parameters:
      - in: query
        name: achievement
        description: Unique URL to the achievement
      - in: path
        name: application
        description: Represents the ID of the application object
      responses:
        200:
          description: OK
      tags:
      - Application
      - Achievements
  /{checkin}:
    get:
      summary: Get Checkin
      description: Represents a single visit by a user to a location
      operationId: getCheckin
      x-api-path-slug: checkin-get
      parameters:
      - in: path
        name: checkin
        description: Represents the ID of the checkin object
      responses:
        200:
          description: OK
      tags:
      - Checkin
  /{checkin}/comments:
    get:
      summary: Get Checkin Comments
      description: All of the comments on this checkin.
      operationId: getCheckinComments
      x-api-path-slug: checkincomments-get
      parameters:
      - in: path
        name: checkin
        description: Represents the ID of the checkin object
      responses:
        200:
          description: OK
      tags:
      - Checkin
      - Comments
    post:
      summary: Post Checkin Comments
      description: Posts a comment to this checkin.
      operationId: postCheckinComments
      x-api-path-slug: checkincomments-post
      parameters:
      - in: path
        name: checkin
        description: Represents the ID of the checkin object
      - in: query
        name: message
        description: Comment text
      responses:
        200:
          description: OK
      tags:
      - Checkin
      - Comments
  /{checkin}/likes:
    get:
      summary: Get Checkin Likes
      description: Users who like this checkin.
      operationId: getCheckinLikes
      x-api-path-slug: checkinlikes-get
      parameters:
      - in: path
        name: checkin
        description: Represents the ID of the checkin object
      responses:
        200:
          description: OK
      tags:
      - Checkin
      - Likes
    post:
      summary: Post Checkin Likes
      description: Likes this checkin.
      operationId: postCheckinLikes
      x-api-path-slug: checkinlikes-post
      parameters:
      - in: path
        name: checkin
        description: Represents the ID of the checkin object
      responses:
        200:
          description: OK
      tags:
      - Checkin
      - Likes
    delete:
      summary: Delete Checkin Likes
      description: Unlikes this checkin.
      operationId: deleteCheckinLikes
      x-api-path-slug: checkinlikes-delete
      parameters:
      - in: path
        name: checkin
        description: Represents the ID of the checkin object
      responses:
        200:
          description: OK
      tags:
      - Checkin
      - Likes
  /{comment}:
    get:
      summary: Get Comment
      description: Returns a comment
      operationId: getComment
      x-api-path-slug: comment-get
      parameters:
      - in: path
        name: comment
        description: Represents the ID of the comment object
      responses:
        200:
          description: OK
      tags:
      - Comment
    delete:
      summary: Delete Comment
      description: Deletes a comment
      operationId: deleteComment
      x-api-path-slug: comment-delete
      parameters:
      - in: path
        name: comment
        description: Represents the ID of the comment object
      responses:
        200:
          description: OK
      tags:
      - Comment
  /{comment}/likes:
    get:
      summary: Get Comment Likes
      description: All the likes on this comment
      operationId: getCommentLikes
      x-api-path-slug: commentlikes-get
      parameters:
      - in: path
        name: comment
        description: Represents the ID of the comment object
      responses:
        200:
          description: OK
      tags:
      - Comment
      - Likes
    post:
      summary: Post Comment Likes
      description: Likes the comment
      operationId: postCommentLikes
      x-api-path-slug: commentlikes-post
      parameters:
      - in: path
        name: comment
        description: Represents the ID of the comment object
      responses:
        200:
          description: OK
      tags:
      - Comment
      - Likes
    delete:
      summary: Delete Comment Likes
      description: Unlikes the comment
      operationId: deleteCommentLikes
      x-api-path-slug: commentlikes-delete
      parameters:
      - in: path
        name: comment
        description: Represents the ID of the comment object
      responses:
        200:
          description: OK
      tags:
      - Comment
      - Likes
  /{event}:
    get:
      summary: Get Event
      description: Specifies information about an event, including the location, event
        name, and which invitees plan to attend.
      operationId: getEvent
      x-api-path-slug: event-get
      parameters:
      - in: path
        name: event
        description: Represents the ID of the event object
      responses:
        200:
          description: OK
      tags:
      - Event
  /{event}/feed:
    get:
      summary: Get Event Feed
      description: This event's wall
      operationId: getEventFeed
      x-api-path-slug: eventfeed-get
      parameters:
      - in: path
        name: event
        description: Represents the ID of the event object
      responses:
        200:
          description: OK
      tags:
      - Event
      - Feed
    post:
      summary: Post Event Feed
      description: Posts a status message on this event's wall
      operationId: postEventFeed
      x-api-path-slug: eventfeed-post
      parameters:
      - in: path
        name: event
        description: Represents the ID of the event object
      - in: query
        name: message
        description: Status Message content
      responses:
        200:
          description: OK
      tags:
      - Event
      - Feed
  /{event}/noreply:
    get:
      summary: Get Event Noreply
      description: All of the users who have been not yet responded to their invitation
        to this event
      operationId: getEventNoreply
      x-api-path-slug: eventnoreply-get
      parameters:
      - in: path
        name: event
        description: Represents the ID of the event object
      responses:
        200:
          description: OK
      tags:
      - Event
      - Noreply
  /{event}/maybe:
    get:
      summary: Get Event Maybe
      description: All of the users who have been responded "Maybe" to their invitation
        to this event
      operationId: getEventMaybe
      x-api-path-slug: eventmaybe-get
      parameters:
      - in: path
        name: event
        description: Represents the ID of the event object
      responses:
        200:
          description: OK
      tags:
      - Event
      - Maybe
    post:
      summary: Post Event Maybe
      description: RSVPs the user as a 'maybe' for the event
      operationId: postEventMaybe
      x-api-path-slug: eventmaybe-post
      parameters:
      - in: path
        name: event
        description: Represents the ID of the event object
      responses:
        200:
          description: OK
      tags:
      - Event
      - Maybe
  /{event}/invited:
    get:
      summary: Get Event Invited
      description: All of the users who have been invited to this event
      operationId: getEventInvited
      x-api-path-slug: eventinvited-get
      parameters:
      - in: path
        name: event
        description: Represents the ID of the event object
      responses:
        200:
          description: OK
      tags:
      - Event
      - Invited
  /{event}/attending:
    get:
      summary: Get Event Attending
      description: All of the users who are attending this event
      operationId: getEventAttending
      x-api-path-slug: eventattending-get
      parameters:
      - in: path
        name: event
        description: Represents the ID of the event object
      responses:
        200:
          description: OK
      tags:
      - Event
      - Attending
    post:
      summary: Post Event Attending
      description: RSVPs the user as 'attending' for the event
      operationId: postEventAttending
      x-api-path-slug: eventattending-post
      parameters:
      - in: path
        name: event
        description: Represents the ID of the event object
      responses:
        200:
          description: OK
      tags:
      - Event
      - Attending
  /{event}/declined:
    get:
      summary: Get Event Declined
      description: All of the users who declined their invitation to this event
      operationId: getEventDeclined
      x-api-path-slug: eventdeclined-get
      parameters:
      - in: path
        name: event
        description: Represents the ID of the event object
      responses:
        200:
          description: OK
      tags:
      - Event
      - Declined
    post:
      summary: Post Event Declined
      description: RSVPs the user as 'declined' for the event
      operationId: postEventDeclined
      x-api-path-slug: eventdeclined-post
      parameters:
      - in: path
        name: event
        description: Represents the ID of the event object
      responses:
        200:
          description: OK
      tags:
      - Event
      - Declined
  /{event}/picture:
    get:
      summary: Get Event Picture
      description: The event's profile picture
      operationId: getEventPicture
      x-api-path-slug: eventpicture-get
      parameters:
      - in: path
        name: event
        description: Represents the ID of the event object
      - in: query
        name: type
        description: One of square (50x50), small (50 pixels wide, variable height),
          and large (about 200 pixels wide,                                                        variable
          height)
      responses:
        200:
          description: OK
      tags:
      - Event
      - Picture
  /{friendlist}:
    get:
      summary: Get Friendlist
      description: A Facebook friend list. This object represents the list itself
        and not the members of the list.
      operationId: getFriendlist
      x-api-path-slug: friendlist-get
      parameters:
      - in: path
        name: friendlist
        description: Represents the ID of the FriendList object
      responses:
        200:
          description: OK
      tags:
      - Friendlist
    delete:
      summary: Delete Friendlist
      description: Deletes the FriendList.
      operationId: deleteFriendlist
      x-api-path-slug: friendlist-delete
      parameters:
      - in: path
        name: friendlist
        description: Represents the ID of the FriendList object
      responses:
        200:
          description: OK
      tags:
      - Friendlist
  /{friendlist}/members:
    get:
      summary: Get Friendlist Members
      description: All of the users who are members of this list.
      operationId: getFriendlistMembers
      x-api-path-slug: friendlistmembers-get
      parameters:
      - in: path
        name: friendlist
        description: Represents the ID of the FriendList object
      responses:
        200:
          description: OK
      tags:
      - Friendlist
      - Members
  /{friendlist}/members/{user}:
    post:
      summary: Post Friendlist Members User
      description: Adds a user to the friend list
      operationId: postFriendlistMembersUser
      x-api-path-slug: friendlistmembersuser-post
      parameters:
      - in: path
        name: friendlist
        description: Represents the ID of the FriendList object
      - in: path
        name: user
        description: Represents the ID of the User to add to or remove from the friend
          list
      responses:
        200:
          description: OK
      tags:
      - Friendlist
      - Members
      - User
    delete:
      summary: Delete Friendlist Members User
      description: Removes a user from the friend list
      operationId: deleteFriendlistMembersUser
      x-api-path-slug: friendlistmembersuser-delete
      parameters:
      - in: path
        name: friendlist
        description: Represents the ID of the FriendList object
      - in: path
        name: user
        description: Represents the ID of the User to add to or remove from the friend
          list
      responses:
        200:
          description: OK
      tags:
      - Friendlist
      - Members
      - User
  /{group}:
    get:
      summary: Get Group
      description: A Facebook group
      operationId: getGroup
      x-api-path-slug: group-get
      parameters:
      - in: path
        name: group
        description: Represents the ID of the group object
      responses:
        200:
          description: OK
      tags:
      - Group
  /{group}/feed:
    get:
      summary: Get Group Feed
      description: This group's wall
      operationId: getGroupFeed
      x-api-path-slug: groupfeed-get
      parameters:
      - in: path
        name: group
        description: Represents the ID of the group object
      responses:
        200:
          description: OK
      tags:
      - Group
      - Feed
    post:
      summary: Post Group Feed
      description: Posts a status message on this group's wall
      operationId: postGroupFeed
      x-api-path-slug: groupfeed-post
      parameters:
      - in: path
        name: group
        description: Represents the ID of the group object
      - in: query
        name: message
        description: Status Message content
      responses:
        200:
          description: OK
      tags:
      - Group
      - Feed
  /{group}/members:
    get:
      summary: Get Group Members
      description: All of the users who are members of this group
      operationId: getGroupMembers
      x-api-path-slug: groupmembers-get
      parameters:
      - in: path
        name: group
        description: Represents the ID of the group object
      responses:
        200:
          description: OK
      tags:
      - Group
      - Members
  /{group}/picture:
    get:
      summary: Get Group Picture
      description: The profile picture of this group
      operationId: getGroupPicture
      x-api-path-slug: grouppicture-get
      parameters:
      - in: path
        name: group
        description: Represents the ID of the group object
      - in: query
        name: type
        description: One of square (50x50), small (50 pixels wide, variable height),
          and large (about 200 pixels wide,                                                        variable
          height)
      responses:
        200:
          description: OK
      tags:
      - Group
      - Picture
  /{group}/docs:
    get:
      summary: Get Group Docs
      description: The docs in this group
      operationId: getGroupDocs
      x-api-path-slug: groupdocs-get
      parameters:
      - in: path
        name: group
        description: Represents the ID of the group object
      responses:
        200:
          description: OK
      tags:
      - Group
      - Docs
  /{link}:
    get:
      summary: Get Link
      description: A link shared on a user's wall
      operationId: getLink
      x-api-path-slug: link-get
      parameters:
      - in: path
        name: link
        description: Represents the ID of the link object
      responses:
        200:
          description: OK
      tags:
      - Link
  /{link}/comments:
    get:
      summary: Get Link Comments
      description: All of the comments on this link.
      operationId: getLinkComments
      x-api-path-slug: linkcomments-get
      parameters:
      - in: path
        name: link
        description: Represents the ID of the link object
      responses:
        200:
          description: OK
      tags:
      - Link
      - Comments
    post:
      summary: Post Link Comments
      description: Posts a comment to this link.
      operationId: postLinkComments
      x-api-path-slug: linkcomments-post
      parameters:
      - in: path
        name: link
        description: Represents the ID of the link object
      - in: query
        name: message
        description: Comment text
      responses:
        200:
          description: OK
      tags:
      - Link
      - Comments
  /{link}/likes:
    get:
      summary: Get Link Likes
      description: Users who like this link.
      operationId: getLinkLikes
      x-api-path-slug: linklikes-get
      parameters:
      - in: path
        name: link
        description: Represents the ID of the link object
      responses:
        200:
          description: OK
      tags:
      - Link
      - Likes
    post:
      summary: Post Link Likes
      description: Likes this link.
      operationId: postLinkLikes
      x-api-path-slug: linklikes-post
      parameters:
      - in: path
        name: link
        description: Represents the ID of the link object
      responses:
        200:
          description: OK
      tags:
      - Link
      - Likes
    delete:
      summary: Delete Link Likes
      description: Unlikes this link.
      operationId: deleteLinkLikes
      x-api-path-slug: linklikes-delete
      parameters:
      - in: path
        name: link
        description: Represents the ID of the link object
      responses:
        200:
          description: OK
      tags:
      - Link
      - Likes
  /{note}:
    get:
      summary: Get Note
      description: A Facebook note
      operationId: getNote
      x-api-path-slug: note-get
      parameters:
      - in: path
        name: note
        description: Represents the ID of the note object
      responses:
        200:
          description: OK
      tags:
      - Note
  /{note}/comments:
    get:
      summary: Get Note Comments
      description: All of the comments on this note.
      operationId: getNoteComments
      x-api-path-slug: notecomments-get
      parameters:
      - in: path
        name: note
        description: Represents the ID of the note object
      responses:
        200:
          description: OK
      tags:
      - Note
      - Comments
    post:
      summary: Post Note Comments
      description: Posts a comment to this note.
      operationId: postNoteComments
      x-api-path-slug: notecomments-post
      parameters:
      - in: query
        name: message
        description: Comment text
      - in: path
        name: note
        description: Represents the ID of the note object
      responses:
        200:
          description: OK
      tags:
      - Note
      - Comments
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