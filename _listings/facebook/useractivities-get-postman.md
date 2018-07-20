{
  "info": {
    "name": "Facebook Get User Activities",
    "_postman_id": "84099341-6804-4fa4-9c1a-abb22a41ab32",
    "description": "The activities listed on the user's profile",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "User",
      "item": [
        {
          "id": "4313fc42-ef22-4101-ae3a-0c9c6173b02e",
          "name": "getUserActivities",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":user/activities"
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
            "description": "The activities listed on the user's profile"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ba7f5902-73bf-4521-b25f-65a73f770057"
            }
          ]
        }
      ]
    }
  ]
}