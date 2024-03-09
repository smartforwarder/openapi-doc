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
  "success": true
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
