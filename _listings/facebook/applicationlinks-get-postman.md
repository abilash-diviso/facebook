{
  "info": {
    "name": "Facebook Get Application Links",
    "_postman_id": "32c5fd5f-e3cb-4635-840d-cc76caae5045",
    "description": "The application's posted links.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Application",
      "item": [
        {
          "id": "6c330d2f-be2e-4ed8-a8b3-4557bde0edee",
          "name": "getApplicationLinks",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":application/links"
              ],
              "variable": [
                {
                  "id": "application",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The application's posted links."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1e9e3df2-fe1f-4b78-9a9d-8ee5125fe0b8"
            }
          ]
        }
      ]
    }
  ]
}