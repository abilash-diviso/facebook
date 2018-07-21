{
  "info": {
    "name": "Facebook Get User Groups",
    "_postman_id": "43af4dad-8c8e-45e1-8992-7c519ffa6d8d",
    "description": "The Groups that the user belongs to.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Page",
      "item": [
        {
          "id": "867b8099-1153-468d-8c95-d2948b6bb383",
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
              "id": "05100db0-5f7b-4df9-9ae9-f9bb1c2553b1"
            }
          ]
        }
      ]
    },
    {
      "name": "User",
      "item": [
        {
          "id": "20601a92-c3c4-4ee0-b994-d3f6b2291f86",
          "name": "getUserGroups",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":user/groups"
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
            "description": "The Groups that the user belongs to."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0c9171ef-2dc8-4281-99cc-9ceae75dce4f"
            }
          ]
        }
      ]
    }
  ]
}