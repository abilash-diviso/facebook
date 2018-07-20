{
  "info": {
    "name": "Facebook Get User Music",
    "_postman_id": "58f7c162-c9df-471e-8b70-ab7546355be1",
    "description": "The music listed on the user's profile",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "User",
      "item": [
        {
          "id": "6b817731-16f8-4e27-9ff5-c2d9e59f4d98",
          "name": "getUserMusic",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":user/music"
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
            "description": "The music listed on the user's profile"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4feb57ee-de73-4955-9f20-8ad41380fef2"
            }
          ]
        }
      ]
    }
  ]
}