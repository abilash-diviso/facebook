{
  "info": {
    "name": "Facebook Get User Notifications",
    "_postman_id": "75a08297-f18b-4eac-afdd-2b181585f9e7",
    "description": "The user's notifications",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "User",
      "item": [
        {
          "id": "fd07f90b-785a-4975-a20a-28f6590a2fd2",
          "name": "getUserNotifications",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":user/notifications"
              ],
              "query": [
                {
                  "key": "include_read",
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
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The user's notifications"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "828ba827-58cb-48bd-adc8-34bafb7cbed3"
            }
          ]
        }
      ]
    }
  ]
}