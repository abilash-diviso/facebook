{
  "info": {
    "name": "Facebook Get Application Albums",
    "_postman_id": "d83d57c1-d9ae-4e38-86a9-183795957ab9",
    "description": "The photo albums this application has created.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Application",
      "item": [
        {
          "id": "05fce4f5-19de-4290-9d60-a4bac5d558e5",
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
              "id": "a1f7117c-fe56-4d54-8503-4da8040b222e"
            }
          ]
        }
      ]
    }
  ]
}