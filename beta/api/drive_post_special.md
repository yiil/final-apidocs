# Create special

Use this API to create a new special.
### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /drive/special
POST /drives/<id>/special
POST /users/<objectId>/drive/special

```
### Request headers
| Name       | Type | Description|
|:---------------|:--------|:----------|
| Authorization  | string  | Bearer <token>. Required. |

### Request body
In the request body, supply a JSON representation of [item](../resources/item.md) object.


### Response
If successful, this method returns `201, Created` response code and [item](../resources/item.md) object in the response body.

### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "create_driveitem_from_drive"
}-->
```http
POST https://graph.microsoft.com/beta/drive/special
Content-type: application/json
Content-length: 504

{
  "driveItem": {
    "content": "content-value",
    "createdBy": {
      "application": {
        "displayName": "displayName-value",
        "id": "id-value"
      },
      "device": {
        "displayName": "displayName-value",
        "id": "id-value"
      },
      "user": {
        "displayName": "displayName-value",
        "id": "id-value"
      }
    },
    "createdDateTime": "datetime-value",
    "cTag": "cTag-value",
    "description": "description-value",
    "eTag": "eTag-value"
  }
}
```
In the request body, supply a JSON representation of [driveItem](../resources/driveitem.md) object.
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.driveitem"
} -->
```http
Content-type: application/json
Content-length: 504

{
  "driveItem": {
    "content": "content-value",
    "createdBy": {
      "application": {
        "displayName": "displayName-value",
        "id": "id-value"
      },
      "device": {
        "displayName": "displayName-value",
        "id": "id-value"
      },
      "user": {
        "displayName": "displayName-value",
        "id": "id-value"
      }
    },
    "createdDateTime": "datetime-value",
    "cTag": "cTag-value",
    "description": "description-value",
    "eTag": "eTag-value"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create special",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->