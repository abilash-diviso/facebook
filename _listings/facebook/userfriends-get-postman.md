{
  "info": {
    "name": "Facebook Get User Friends",
    "_postman_id": "35f9d193-a157-4723-9d25-9fd797aa428a",
    "description": "The user's friends",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "User",
      "item": [
        {
          "id": "5139ea7c-22a0-4220-a388-3af6b276fafb",
          "name": "getUserFriends",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":user/friends"
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
            "description": "The user's friends"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c3eebb19-1fdd-4ef3-9c10-67d24b58f2b1"
            }
          ]
        }
      ]
    }
  ]
}