{
  "info": {
    "name": "Facebook Post Event Declined",
    "_postman_id": "3c177e6b-9196-43ca-a8f7-45de29e72236",
    "description": "RSVPs the user as 'declined' for the event",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Event",
      "item": [
        {
          "id": "3b32ab58-ccbb-4e2a-a301-345b56c248b8",
          "name": "getEventDeclined",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":event/declined"
              ],
              "variable": [
                {
                  "id": "event",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "All of the users who declined their invitation to this event"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "fcaeb28e-3213-411f-964d-d39c67b5fcc0"
            }
          ]
        },
        {
          "id": "b19ae748-a3f4-4656-b9c2-0cf34ca7263a",
          "name": "postEventDeclined",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":event/declined"
              ],
              "variable": [
                {
                  "id": "event",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "RSVPs the user as 'declined' for the event"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ceb71049-03b8-4b5a-aad8-9ab85befd029"
            }
          ]
        }
      ]
    }
  ]
}