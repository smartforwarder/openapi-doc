# SmartForwarder OpenAPI Document 

## Login and health check APIs

Please check the login and health APIs in the root directory README.md.

## Shipments API

### Get shipments

**URL** : `/v1/shipments`

**Method** : `GET`

**Auth required** : YES

**API call**
```
GET {{baseUrl}}/v1/shipments
Authorization: Bearer {{token}}
Content-Type: application/json
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "success": true
}
```
### Get A Shipment

**URL** : `/v1/shipments/:id`

**Method** : `GET`

**Auth required** : YES

**API call**
```
GET {{baseUrl}}/v1/shipments/:id
Authorization: Bearer {{token}}
Content-Type: application/json
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "success": true
}
```

### Create A Shipment

**URL** : `/v1/shipments`

**Method** : `POST`

**Auth required** : YES

**API call**
```
POST {{baseUrl}}/v1/shipments
Authorization: Bearer {{token}}
Content-Type: application/json
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "success": true
}
```

### Update A Shipment

**URL** : `/v1/shipments/:id`

**Method** : `PUT`

**Auth required** : YES

**API call**
```
PUT {{baseUrl}}/v1/shipments/:id
Authorization: Bearer {{token}}
Content-Type: application/json
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "success": true
}
```

### Delete A Shipment

**URL** : `/v1/shipments/:id`

**Method** : `DELETE`

**Auth required** : YES

**API call**
```
DELETE {{baseUrl}}/v1/shipments/:id
Authorization: Bearer {{token}}
Content-Type: application/json
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "success": true
}
```

### Create Documents For A Shipment

**URL** : `/v1/shipments/:id/documents`

**Method** : `POST`

**Auth required** : YES

**API call**
```
POST {{baseUrl}}/v1/shipments/:id/documents
Authorization: Bearer {{token}}
Content-Type: application/json
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "success": true
}
```

### Find Documents For A Shipment

**URL** : `/v1/shipments/:id/documents`

**Method** : `GET`

**Auth required** : YES

**API call**
```
GET {{baseUrl}}/v1/shipments/:id/documents
Authorization: Bearer {{token}}
Content-Type: application/json
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "success":true,
  "data":[
    {
      "ext_id":"5a4083de-51c5-4f5a-8a3d-fd2854a29d10",
      "name":"交接单",
      "files":[
        {
          "id":18770,
          "name":"交接单.pdf",
          "alternativeText":null,
          "caption":null,
          "width":null,
          "height":null,
          "formats":null,
          "hash":"HASLC_01240115829_DOE_24011042_288895e81a",
          "ext":".pdf",
          "mime":"application/pdf",
          "size":383.27,
          "url":"https://yahoo.com/assets/HASLC_01240115829_DOE_24011042_288895e81a.pdf",
          "previewUrl":null,
          "provider":"oss",
          "provider_metadata":null,
          "created_by":null,
          "updated_by":null,
          "created_at":"2024-02-25T21:31:26.000Z",
          "updated_at":"2024-02-25T21:31:26.000Z"
        }
      ],
      "private":false
    }
  ]
}
```

## Documents API

### Update A Document

**URL** : `/v1/documents/:id`

**Method** : `PUT`

**Auth required** : YES

**API call**
```
PUT {{baseUrl}}/v1/documents/:id
Authorization: Bearer {{token}}
Content-Type: application/json
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "success": true
}
```

### Delete A Document 

**URL** : `/v1/documents/:id`

**Method** : `DELETE`

**Auth required** : YES

**API call**
```
DELETE {{baseUrl}}/v1/documents/:id
Authorization: Bearer {{token}}
Content-Type: application/json
```

**Success Response**

**Code** : `200 OK`

**Content example**

```json
{
  "success": true
}
```
