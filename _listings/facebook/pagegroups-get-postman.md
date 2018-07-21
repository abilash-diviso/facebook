{
  "info": {
    "name": "Facebook Get Page Groups",
    "_postman_id": "c2fd9b94-53e6-47c7-b3e4-bafa73d4e637",
    "description": "The groups this page is a member of",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Page",
      "item": [
        {
          "id": "3fed59dd-a2fd-4650-a443-bfc1e10026e8",
          "name": "getPageGroups",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":page/groups"
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
            "description": "The groups this page is a member of"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bb0cbeb6-d806-4022-9a4c-43b0b3c32353"
            }
          ]
        }
      ]
    }
  ]
}