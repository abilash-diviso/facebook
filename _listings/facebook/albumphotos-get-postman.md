{
  "info": {
    "name": "Facebook Get Album Photos",
    "_postman_id": "1d711e00-2303-48e8-8311-5fae0e151b7f",
    "description": "The photos contained in this album",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Album",
      "item": [
        {
          "id": "835fd004-97fd-4d59-9b78-78188df7443e",
          "name": "getAlbumPhotos",
          "request": {
            "url": {
              "protocol": "http",
              "host": "graph.facebook.com",
              "path": [
                ":album/photos"
              ],
              "variable": [
                {
                  "id": "album",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "The photos contained in this album"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b410b696-19cd-4e76-a15d-f745e0373aba"
            }
          ]
        }
      ]
    }
  ]
}