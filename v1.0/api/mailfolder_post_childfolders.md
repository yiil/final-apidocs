# Create MailFolder

Use this API to create a new child mailfolder.
### Prerequisites
One of the following **scopes** is required to execute this API: 
*Mail.ReadWrite*
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /me/mailFolders/<id>/childFolders
POST /users/<id | userPrincipalName>/mailFolders/<id>/childFolders
```
### Request headers
| Header       | Value |
|:---------------|:--------|
| Authorization  | Bearer <token>. Required.  |
| Content-Type  | application/json. Required.  |

### Request body
In the request body, supply a JSON representation of [MailFolder](../resources/mailfolder.md) object.


### Response
If successful, this method returns `201, Created` response code and [MailFolder](../resources/mailfolder.md) object in the response body.

### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "create_mailfolder_from_mailfolder"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/mailFolders/<id>/childFolders
Content-type: application/json
Content-length: 159

{
  "displayName": "displayName-value",
  "parentFolderId": "parentFolderId-value",
  "childFolderCount": 99,
  "unreadItemCount": 99,
  "totalItemCount": 99
}
```
In the request body, supply a JSON representation of [mailFolder](../resources/mailfolder.md) object.
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailfolder"
} -->
```http
Content-type: application/json
Content-length: 179

{
  "displayName": "displayName-value",
  "parentFolderId": "parentFolderId-value",
  "childFolderCount": 99,
  "unreadItemCount": 99,
  "totalItemCount": 99,
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create MailFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->