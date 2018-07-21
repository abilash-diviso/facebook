{
  "info": {
    "name": "Facebook Get Application Staticresources",
    "_postman_id": "ac318f0d-955a-4159-8989-652069dc90e3",
    "description": "Usage stats about the canvas application's static resources, such as javascript and CSS, and which ones are being flushed to browsers early.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Application",
      "item": [
        {
          "id": "cbd54f71-ca00-4b03-a9ab-edd3115af97e",
          "name": "getApplicationStaticresources",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":application/staticresources"
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
            "description": "Usage stats about the canvas application's static resources, such as javascript and CSS, and which ones are being flushed to browsers early."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b2cefaff-2902-4836-9026-14af8aeb242b"
            }
          ]
        }
      ]
    }
  ]
}