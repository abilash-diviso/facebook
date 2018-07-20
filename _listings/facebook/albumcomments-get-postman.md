{
  "info": {
    "name": "Facebook Get Album Comments",
    "_postman_id": "1d8ebc4e-09c7-4f1a-8f75-71cd64b9c99a",
    "description": "The comments made on this album",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Album",
      "item": [
        {
          "id": "96b75550-1a32-4aba-81c0-8bd69d6bb275",
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
              "id": "12f31bfb-088e-4a84-86ad-8bc4c7cfa5cf"
            }
          ]
        }
      ]
    }
  ]
}