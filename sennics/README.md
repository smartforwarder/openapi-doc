# SmartForwarder OpenAPI Document 

## 工作流程

### CRM 发送订舱委托

- CRM呼叫登录API，获取JWT token
- CRM呼叫订舱委托单推送接⼝(createshipment API)
- ⽤户在SF货代系统中进⾏确认
- 确认后，SF呼叫CRM订舱回执推送接⼝来提供相关信息

### CRM 更改订舱委托

- CRM呼叫登录API，获取JWT token
- CRM呼叫findShipments接⼝获取shipment id
- CRM呼叫订舱委托单更新接⼝(updateshipment API)
- ⽤户在SF货代系统中进⾏确认
- 确认后，SF呼叫CRM订舱回执变更/删除接⼝来提供相关信息

### 货代更改订舱委托

- ⽤户在SF货代系统中进⾏修改
- 确认后，SF呼叫CRM订舱回执变更/删除接⼝来提供相关信息

### CRM 删除订舱委托

- CRM呼叫登录API，获取JWT token
- CRM呼叫findShipments接⼝获取shipment id
- CRM呼叫订舱委托单删除接⼝(deleteshipment API)
- ⽤户在SF货代系统中进⾏确认
- 确认后，SF呼叫CRM订舱回执变更/删除接⼝来提供相关信息

### CRM 发送报关单据

- CRM呼叫登录API，获取JWT token
- CRM呼叫findShipments接⼝获取shipment id
- CRM呼叫报关单据推送接⼝(createshipment document API)
- ⽤户在SF货代系统中进⾏确认
- 确认后，SF调⽤报关单据变更接⼝通知CRM ？？？

### CRM 修改报关单据

- CRM呼叫登录API，获取JWT token
- CRM呼叫findShipments接⼝获取shipment id
- CRM呼叫报关单据修改接⼝(updatedocument API)
- ⽤户在SF货代系统中进⾏确认
- 确认后，SF调⽤报关单据变更接⼝通知CRM ？？？

### CRM 删除报关单据

- CRM呼叫登录API，获取JWT token
- CRM呼叫findShipments接⼝获取shipment id
- CRM呼叫报关单据删除接⼝(deletedocument API)
- ⽤户在SF货代系统中进⾏确认
- 确认后，SF调⽤报关单据变更接⼝通知CRM ？？？

### CRM 查询物流状态跟踪

- CRM呼叫登录API，获取JWT token
- CRM呼叫findShipments接⼝获取所有shipments的物流状态


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
{{
  "success":true,
  "total":45,
  "data":[
    {
      "ext_id":"a06019af-959a-440a-ac0e-fd4f90c13f9a",
      "created_at":"2024-01-25T19:25:47.000Z",
      "updated_at":"2024-03-05T03:13:17.000Z",
      "shipment_number":"DOE011040"
    },
    {
      "ext_id":"e5686667-4784-4d55-be79-45401aa371c4",
      "created_at":"2024-01-25T18:35:32.000Z",
      "updated_at":"2024-03-04T19:27:24.000Z",
      "shipment_number":"DOE011038"
    },
    {
      "ext_id":"af052184-8e57-4e9e-a08a-1052caa3e140",
      "created_at":"2024-01-25T18:53:14.000Z",
      "updated_at":"2024-03-04T01:44:41.000Z",
      "shipment_number":"DOE011039"
    },
    {
      "ext_id":"bd837c1c-be72-4611-8acc-e59e14484a71",
      "created_at":"2024-01-22T22:17:07.000Z",
      "updated_at":"2024-03-03T19:54:00.000Z",
      "shipment_number":"DOE011033"
    },
    {
      "ext_id":"f5bb3ed4-e5ef-481c-b851-f389137494e0",
      "created_at":"2023-12-28T02:55:00.000Z",
      "updated_at":"2024-03-03T19:51:12.000Z",
      "shipment_number":"DOE120022"
    }
  ]
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
  "success":true,
  "data":{
    "ext_id":"0d127e6f-f140-4a64-9222-f565c8fcb65d",
    "created_at":"2024-01-29T01:07:41.000Z",
    "updated_at":"2024-02-28T04:24:48.000Z",
    "shipment_number":"DOE24011042"
  }
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
