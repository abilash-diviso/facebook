{
  "info": {
    "name": "Facebook Get Event Declined",
    "_postman_id": "51ac50d6-ffa0-4eb6-9967-2cc61be19d8f",
    "description": "All of the users who declined their invitation to this event",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Event",
      "item": [
        {
          "id": "77ee0d78-7583-4934-8f83-e9eead8ad45b",
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
              "id": "9ae1cada-7061-4104-8f97-2036bab35764"
            }
          ]
        }
      ]
    }
  ]
}