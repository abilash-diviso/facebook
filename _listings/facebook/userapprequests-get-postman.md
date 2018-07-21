{
  "info": {
    "name": "Facebook Get User Apprequests",
    "_postman_id": "8242862a-c368-434c-8f1c-a46639076ff8",
    "description": "The user's outstanding requests from an app.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "User",
      "item": [
        {
          "id": "f86d2475-2857-412e-aa87-ad403616172c",
          "name": "getUserApprequests",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":user/apprequests"
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
            "description": "The user's outstanding requests from an app."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "96479110-10fa-4d51-ac90-cc5551f75c53"
            }
          ]
        }
      ]
    }
  ]
}