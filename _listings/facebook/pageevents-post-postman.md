{
  "info": {
    "name": "Facebook Post Page Events",
    "_postman_id": "10074a6a-8bb9-4f2d-840c-f6eabd24d418",
    "description": "Creates an event for the page",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Page",
      "item": [
        {
          "id": "a45067d3-8f1c-4b15-b2a0-84e4bd97f93a",
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
              "id": "e35cdbfb-cac5-42ed-a3c8-006f38883281"
            }
          ]
        },
        {
          "id": "14d170c3-da7e-46f3-bf8e-ff1bbc4671de",
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
              "id": "0511f3f8-16d8-437b-9b6a-32279a6fe694"
            }
          ]
        }
      ]
    }
  ]
}