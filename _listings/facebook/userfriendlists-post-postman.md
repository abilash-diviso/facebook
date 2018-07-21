{
  "info": {
    "name": "Facebook Post User Friendlists",
    "_postman_id": "54fd581a-75f1-47dd-8b57-7d5003f3fe07",
    "description": "Creates a FriendList for the user",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "User",
      "item": [
        {
          "id": "9491e9f3-74b4-4644-a99a-3dda8606a80f",
          "name": "postUserFriendlists",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":user/friendlists"
              ],
              "query": [
                {
                  "key": "name",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "user",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a FriendList for the user"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b1bb0923-c4b4-4520-b4b7-2b2c9b12932a"
            }
          ]
        }
      ]
    }
  ]
}