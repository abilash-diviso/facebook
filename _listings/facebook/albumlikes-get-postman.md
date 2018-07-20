{
  "info": {
    "name": "Facebook Get Album Likes",
    "_postman_id": "64948ae6-87e4-468c-ac92-a05bb603bfe6",
    "description": "The likes made on this album",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Search",
      "item": [
        {
          "id": "4377b048-4d26-433f-936b-d6db675b6df5",
          "name": "getSearch",
          "request": {
            "url": "http://graph.facebook.com/search?q=%7B%7D&type=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Search over all public objects in the social graph"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "206cf67f-bb73-41eb-bf05-af61a198288a"
            }
          ]
        }
      ]
    },
    {
      "name": "Album",
      "item": [
        {
          "id": "00950809-fe2d-48b6-bc78-64cadf0bea03",
          "name": "getAlbum",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":album"
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
            "description": "A photo album"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c509e1cf-75e3-46fc-9a1f-f2cf6ae3bcdf"
            }
          ]
        },
        {
          "id": "543f35e6-039c-46b7-9466-2de5426e60d8",
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
              "id": "336094c2-2cee-40be-b48a-5f72a480a593"
            }
          ]
        },
        {
          "id": "74667359-8ac2-4759-bad1-adc8611b2e98",
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
              "id": "86b1339e-b2ac-4fbb-b7e3-87af0abe6c72"
            }
          ]
        },
        {
          "id": "1b167968-4e52-43db-b106-beba03192eca",
          "name": "getAlbumLikes",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":album/likes"
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
            "description": "The likes made on this album"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a7c5f788-6b87-4486-bcc0-449a412b3e4b"
            }
          ]
        }
      ]
    }
  ]
}