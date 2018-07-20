{
  "info": {
    "name": "Facebook Get User Adds",
    "_postman_id": "03b9058c-bfba-4d6d-a00d-e6fae0998a8b",
    "description": "The user's posts",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Application",
      "item": [
        {
          "id": "9acdaa4a-8019-483b-b42f-5df70587cec3",
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
              "id": "d04f5d1c-7a5c-418a-b9fb-ccfc2259af04"
            }
          ]
        }
      ]
    },
    {
      "name": "Page",
      "item": [
        {
          "id": "03960fd2-0daf-4d2a-9def-b2fef61dc9b2",
          "name": "getPageAdds",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":page/posts"
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
            "description": "The page's own posts"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "eeb05336-8c15-4407-b15e-97372ab5d3fa"
            }
          ]
        }
      ]
    },
    {
      "name": "User",
      "item": [
        {
          "id": "42bf1649-1e57-4d20-b837-6c417255daea",
          "name": "getUserAdds",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":user/posts"
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
            "description": "The user's posts"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5ae280be-7515-489d-8279-784dce81a2e1"
            }
          ]
        }
      ]
    }
  ]
}