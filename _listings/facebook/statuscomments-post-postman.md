{
  "info": {
    "name": "Facebook Post Status Comments",
    "_postman_id": "5a728dd5-a95f-41e5-bf69-f94d37eeb276",
    "description": "Posts a comment to this status.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Album",
      "item": [
        {
          "id": "d6d4e0c0-38b8-43fb-8c70-5112b9c3d20d",
          "name": "getAlbumComments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":album/comments"
              ],
              "variable": [
                {
                  "id": "album",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The comments made on this album"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6278ad02-ecb2-4e80-86ea-596d2d24d467"
            }
          ]
        },
        {
          "id": "70ddb217-5c3a-49c4-bef7-f8edb72bb78c",
          "name": "postAlbumComments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":album/comments"
              ],
              "query": [
                {
                  "key": "message",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "album",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Posts a comment on the album"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "70930bf0-fb31-4eb4-b325-106557caeaf1"
            }
          ]
        }
      ]
    },
    {
      "name": "Checkin",
      "item": [
        {
          "id": "991ba0da-e41c-45b0-8dc9-821b3ffcf147",
          "name": "getCheckinComments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":checkin/comments"
              ],
              "variable": [
                {
                  "id": "checkin",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "All of the comments on this checkin."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6911e4e8-b174-49ed-a85f-7b0f76bbed0b"
            }
          ]
        },
        {
          "id": "1196ee0f-cffa-4563-927a-5b2bdea4c97a",
          "name": "postCheckinComments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":checkin/comments"
              ],
              "query": [
                {
                  "key": "message",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "checkin",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Posts a comment to this checkin."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "63757d92-3e9e-48dd-b6b6-81e8cbfe3605"
            }
          ]
        }
      ]
    },
    {
      "name": "Link",
      "item": [
        {
          "id": "8976247b-2399-4d35-843b-3a0faccce2b2",
          "name": "getLinkComments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":link/comments"
              ],
              "variable": [
                {
                  "id": "link",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "All of the comments on this link."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "56c50dcf-3e0f-4aad-b8a5-6241cd1fc380"
            }
          ]
        },
        {
          "id": "53e55b9d-696c-4336-b9a5-d81aa60e229c",
          "name": "postLinkComments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":link/comments"
              ],
              "query": [
                {
                  "key": "message",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "link",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Posts a comment to this link."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "066971fa-4ca5-4572-a2b4-b695f452fd91"
            }
          ]
        }
      ]
    },
    {
      "name": "Note",
      "item": [
        {
          "id": "ee5fab69-be0e-4a05-9943-025362119471",
          "name": "getNoteComments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":note/comments"
              ],
              "variable": [
                {
                  "id": "note",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "All of the comments on this note."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "881a1847-e6ec-4bd0-8ac6-92ddf3a070d9"
            }
          ]
        },
        {
          "id": "3b409398-bd15-43f0-8e9b-7b8b6d71c48e",
          "name": "postNoteComments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":note/comments"
              ],
              "query": [
                {
                  "key": "message",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "note",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Posts a comment to this note."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c1aa74f2-037c-414c-90f6-f8b3ae4a5b90"
            }
          ]
        }
      ]
    },
    {
      "name": "Photo",
      "item": [
        {
          "id": "dd56a06f-e2d4-49d5-ae61-33e4f97cb9d6",
          "name": "getPhotoComments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":photo/comments"
              ],
              "variable": [
                {
                  "id": "photo",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "All of the comments on this photo."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "093d8717-f7bf-4e47-bd85-cfd52cdd04a3"
            }
          ]
        },
        {
          "id": "35274494-b22f-4f63-ba5f-54944ed804f1",
          "name": "postPhotoComments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":photo/comments"
              ],
              "query": [
                {
                  "key": "message",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "photo",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Posts a comment to this photo."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9e0b546e-8ed6-4989-bcee-d8e39f28d4ab"
            }
          ]
        }
      ]
    },
    {
      "name": "Post",
      "item": [
        {
          "id": "a6524db9-d71b-4d2f-81c9-8405e433180b",
          "name": "getAddComments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":post/comments"
              ],
              "variable": [
                {
                  "id": "post",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "All of the comments on this post."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "755c42ac-1bb6-47ef-b188-a55e8025ab09"
            }
          ]
        },
        {
          "id": "91292118-4bd1-4759-8cbd-a9db98c97e42",
          "name": "postAddComments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":post/comments"
              ],
              "query": [
                {
                  "key": "message",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "post",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Posts a comment to this post."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1e6a9b0b-3d2b-40e2-982e-bf9d8e494d32"
            }
          ]
        }
      ]
    },
    {
      "name": "Status",
      "item": [
        {
          "id": "5fa076b6-0f7e-4340-a05d-a338ee719632",
          "name": "getStatusComments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":status/comments"
              ],
              "variable": [
                {
                  "id": "status",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "All of the comments on this status."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3a79e256-679c-4009-9ec8-d82b753e140d"
            }
          ]
        },
        {
          "id": "513f0eb7-bd2a-4f62-b01b-7368670bcc1d",
          "name": "postStatusComments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":status/comments"
              ],
              "query": [
                {
                  "key": "message",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "status",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Posts a comment to this status."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "312fc2f8-0e51-4365-be1b-95ea70acc737"
            }
          ]
        }
      ]
    }
  ]
}