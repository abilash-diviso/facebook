{
  "info": {
    "name": "Facebook Get User Albums",
    "_postman_id": "2774274f-c937-43e7-8891-6ae6da500d01",
    "description": "The photo albums this user has created",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Application",
      "item": [
        {
          "id": "582d2f57-7236-4493-b327-d5ba0efd188c",
          "name": "getApplicationAlbums",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":application/albums"
              ],
              "variable": [
                {
                  "id": "application",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The photo albums this application has created."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c485c3b3-cf32-4d5a-aee0-89a8d1c87c88"
            }
          ]
        }
      ]
    },
    {
      "name": "Page",
      "item": [
        {
          "id": "434dd627-953c-4b05-a90c-1961069362fa",
          "name": "getPageAlbums",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":page/albums"
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
            "description": "The photo albums this Page has uploaded"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3091051e-3703-4400-973b-5947a8968e11"
            }
          ]
        }
      ]
    },
    {
      "name": "User",
      "item": [
        {
          "id": "ae1540b0-df22-4b6b-b8d1-62ddd2426e66",
          "name": "getUserAlbums",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":user/albums"
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
            "description": "The photo albums this user has created"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bfed3d8a-a048-43b3-930c-af09501e8072"
            }
          ]
        }
      ]
    }
  ]
}