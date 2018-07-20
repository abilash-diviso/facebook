{
  "info": {
    "name": "Facebook Get Page Albums",
    "_postman_id": "79a5360f-aa4d-4f5f-8465-ac4a2d0506fb",
    "description": "The photo albums this Page has uploaded",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Application",
      "item": [
        {
          "id": "e7cb3b4a-a23d-4f45-b864-7a44d3a5e4ec",
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
              "id": "266aed6c-f678-4b47-b82b-515f45cc725f"
            }
          ]
        }
      ]
    },
    {
      "name": "Page",
      "item": [
        {
          "id": "11a8ed00-4c1a-43fa-9804-09baa27412e8",
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
              "id": "07b0eb2b-717e-4790-acef-e2c180d8d8d5"
            }
          ]
        }
      ]
    }
  ]
}