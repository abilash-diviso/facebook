{
  "info": {
    "name": "Facebook Get User Friends Friend",
    "_postman_id": "b3854470-9aee-4f2f-b14f-72de8745653c",
    "description": "Checks if the given user is a friend of the current user",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "User",
      "item": [
        {
          "id": "6c118449-dac3-451d-88fd-4ef7ecf4011a",
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
              "id": "d6faf4f6-8b92-4934-bd9c-e8efc76f7dac"
            }
          ]
        },
        {
          "id": "732e1e5f-20d1-47bd-8924-aed680a63177",
          "name": "getUserFriendsFriend",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":user/friends/:friend"
              ],
              "variable": [
                {
                  "id": "friend",
                  "value": "{}",
                  "type": "string"
                },
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
            "description": "Checks if the given user is a friend of the current user"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "e42444e9-6222-435c-9dd3-0facee6d2fc1"
            }
          ]
        }
      ]
    }
  ]
}