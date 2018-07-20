{
  "info": {
    "name": "Facebook Get User Events",
    "_postman_id": "0451b858-1a93-4ed4-bb71-2b7735e515ec",
    "description": "The events this user is attending.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Page",
      "item": [
        {
          "id": "819e9aa1-5894-42fb-a200-fb7d8081acde",
          "name": "getPageEvents",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":page/events"
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
            "description": "The events the Page is attending"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f56e42d3-14c7-4434-b9c0-58c414e4294d"
            }
          ]
        },
        {
          "id": "a6e6706a-f520-48e6-84cb-cb44892e771a",
          "name": "postPageEvents",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":page/events"
              ],
              "query": [
                {
                  "key": "end_time",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "location",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "message",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "name",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "privacy_type",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "start_time",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "page",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Creates an event for the page"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "62e123e1-2355-4cc6-9565-37aeab36dcb8"
            }
          ]
        }
      ]
    },
    {
      "name": "User",
      "item": [
        {
          "id": "a6331afe-b793-4afc-9a95-9dc20ef26ebe",
          "name": "getUserEvents",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":user/events"
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
            "description": "The events this user is attending."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b70a0438-ee32-459d-b187-2e8b57295a46"
            }
          ]
        }
      ]
    }
  ]
}