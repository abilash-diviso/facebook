{
  "info": {
    "name": "Facebook Get Search",
    "_postman_id": "096894ab-cf7e-4586-b3cd-b37c9e9f772d",
    "description": "Search over all public objects in the social graph",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Search",
      "item": [
        {
          "id": "ff6ff264-913e-4439-8f93-c9d6c08f2515",
          "name": "getSearch",
          "request": {
            "url": "http://graph.facebook.com/search?q=%7B%7D&type=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Search over all public objects in the social graph"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c7d7d22f-75f0-4297-ae96-916edbe6f5f8"
            }
          ]
        }
      ]
    }
  ]
}