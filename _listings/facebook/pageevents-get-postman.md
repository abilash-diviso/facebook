{
  "info": {
    "name": "Facebook Get Page Events",
    "_postman_id": "2f81a7ff-f9a5-45e8-a84e-ce3186270881",
    "description": "The events the Page is attending",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Page",
      "item": [
        {
          "id": "e2c4a03b-10f1-4311-84f8-97b4e86eeadf",
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
              "id": "88ac438b-acd0-4686-99a0-766e9920ed3b"
            }
          ]
        }
      ]
    }
  ]
}