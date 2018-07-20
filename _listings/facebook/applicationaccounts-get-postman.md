{
  "info": {
    "name": "Facebook Get Application Accounts",
    "_postman_id": "2b090fce-a44d-478d-8e9b-f79bd7383eda",
    "description": "Test User accounts associated with the application.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Application",
      "item": [
        {
          "id": "784e0752-2a27-4e88-ac49-5802257e53fe",
          "name": "getApplicationAccounts",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":application/accounts"
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
            "description": "Test User accounts associated with the application."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cc5c8f50-15f7-4441-be0a-8d290daaea81"
            }
          ]
        }
      ]
    }
  ]
}