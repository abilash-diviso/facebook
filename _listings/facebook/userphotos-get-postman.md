{
  "info": {
    "name": "Facebook Get User Photos",
    "_postman_id": "55e701db-afcd-4e3a-a5ac-ab2ba5f976b8",
    "description": "The photos the user is tagged in",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Album",
      "item": [
        {
          "id": "1754b2ea-575f-4380-a951-c19569f4c53f",
          "name": "getAlbumPhotos",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":album/photos"
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
            "description": "The photos contained in this album"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "be347bab-b2df-470b-81b6-261cae5d6657"
            }
          ]
        },
        {
          "id": "7bf5d972-272c-458b-9a4c-5601bf746864",
          "name": "postAlbumPhotos",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":album/photos"
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
            "description": "Adds a photo to the album"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4acc3a26-b4be-4e11-aae4-006974fc5443"
            }
          ]
        }
      ]
    },
    {
      "name": "Page",
      "item": [
        {
          "id": "01b6d511-85b9-4297-b1ef-61699c272542",
          "name": "getPagePhotos",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":page/photos"
              ],
              "variable": [
                {
                  "id": "page",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The photos contained on this page"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "83ba9b4c-590b-4eac-b704-530407b5548e"
            }
          ]
        },
        {
          "id": "23044803-b8b7-4181-aceb-570e906c7fbc",
          "name": "postPagePhotos",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":page/photos"
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
                  "id": "page",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Adds a photo to the page"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "76262e35-5537-4465-8cef-bf62478e2c5a"
            }
          ]
        }
      ]
    },
    {
      "name": "User",
      "item": [
        {
          "id": "518f527c-c985-47a8-b1c2-849ef1629a54",
          "name": "getUserPhotos",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":user/photos"
              ],
              "variable": [
                {
                  "id": "user",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The photos the user is tagged in"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "53c74d86-bada-4785-95a6-efbae67c59bb"
            }
          ]
        }
      ]
    }
  ]
}