{
  "info": {
    "name": "Facebook Get Application Adds",
    "_postman_id": "1a671888-04d2-4fb8-aa13-e43f18fc15fa",
    "description": "The application's own posts.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Application",
      "item": [
        {
          "id": "3a145b9b-e4f9-4cf7-b466-1890378decbd",
          "name": "getApplicationAdds",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":application/posts"
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
            "description": "The application's own posts."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "feaabb67-ea3b-4a43-b422-eacfe0e390fc"
            }
          ]
        }
      ]
    }
  ]
}