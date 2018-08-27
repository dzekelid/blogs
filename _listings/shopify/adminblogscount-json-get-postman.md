{
  "info": {
    "name": "Shopify Get a count of all blogs",
    "_postman_id": "205a3426-e688-46ea-8438-8e91ba18b5c2",
    "description": "Get a count of all blogs.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Commerce",
      "item": [
        {
          "id": "faed8313-3e83-4e3e-9e35-7eb14adbcb69",
          "name": "getAdminBlogs.json",
          "request": {
            "url": "http://DefaultParameterValue:DefaultParameterValue@DefaultParameterValue.myshopify.com/admin/blogs.json",
            "method": "GET",
            "header": [
              {
                "key": "Content-Type",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get a list of all blogs."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "de98e9ef-5acc-4d03-be18-da7fba3f148a"
            }
          ]
        },
        {
          "id": "1123505c-5c05-4cee-8a53-9ab2b4cd65fd",
          "name": "getAdminBlogsCount.json",
          "request": {
            "url": "http://DefaultParameterValue:DefaultParameterValue@DefaultParameterValue.myshopify.com/admin/blogs/count.json",
            "method": "GET",
            "header": [
              {
                "key": "Content-Type",
                "value": "{}",
                "description": "",
                "disabled": false
              },
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get a count of all blogs."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c036020d-bd61-41c1-93e3-d388f8f74897"
            }
          ]
        }
      ]
    }
  ]
}