# Get contact

Retrieve the properties and relationships of contact object.
### Prerequisites
One of the following **scopes** is required to execute this API: 
*Contacts.Read; Contacts.ReadWrite*
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /me/contacts/<id>
GET /users/<id>/contacts/<id>
GET /users/<userPrincipalName>/contacts/<id>
GET /me/contactfolders/<contactFolderId>/contacts/<id>
GET /users/<id>/contactfolders/<contactFolderId>/contacts/<id>
GET /users/<userPrincipalName>/contactFolders/<contactFolderId>/contacts/<id>
```
### Optional query parameters
This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.
### Request headers
| Header       | Value |
|:---------------|:--------|
| Authorization  | Bearer %token%  |

### Request body
Do not supply a request body for this method.
### Response
If successful, this method returns a `200 OK` response code and [contact](../resources/contact.md) object in the response body.
### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "get_contact"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contacts/<id>
```
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contact"
} -->
```http
Content-type: application/json
Content-length: 210

{
  "parentFolderId": "parentFolderId-value",
  "birthday": "datetime-value",
  "fileAs": "fileAs-value",
  "displayName": "displayName-value",
  "givenName": "givenName-value",
  "initials": "initials-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get contact",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->