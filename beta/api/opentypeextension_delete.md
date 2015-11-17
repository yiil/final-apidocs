# Delete extension

Delete an open type data extension from the specified instance of a resource. 

The resource can be a message, calendar event, or contact of the signed-in user's on Office 365 or
Outlook.com. Or, it can be an event for an Office 365 group.

### Prerequisites

One of the following **scopes** is required to execute this API, depending on the resource you're
deleting the extension from:

- _Mail.ReadWrite_
- _Calendars.ReadWrite_
- _Contacts.ReadWrite_
- _Group.ReadWrite.All_

 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/messages/<id>/extensions/<eId>
DELETE /users/<objectId>/messages/<id>/extensions/<eId>

DELETE /me/events/<id>/extensions/<eId>
DELETE /users/<objectId>/events/<id>/extensions/<eId>

DELETE /me/contacts/<id>/extensions/<eId>
DELETE /users/<objectId>/contacts/<id>/extensions/<eId>

DELETE /groups/<gId>/events/<id>/extensions/<eId>

```

### Parameters
|**Parameter**|**Type**|**Description**|
|:-----|:-----|:-----|
|_URL parameters_|
|id|string|A unique identifier for an instance of a resource (message, event, or contact). Required.|
|eId|string|This can be an extension name which is a unique text identifier for the extension, or a fully qualified name which concatenates the extension type and unique text identifier. The fully qualified name is returned in the `Id` property when you create the extension. Required.|
|objectId|string|A unique identifier for the signed-in user. Required.|
|gId|string|A unique group ID. Required.|


### Request headers
| Name       | Value |
|:---------------|:----------|
| Authorization | Bearer %token%|


### Request body
Do not supply a request body for this method.


### Response
If successful, this method returns `204, No Content` response code. It does not return anything in the response body.

### Example
##### Request
The first example references an extension by its name and deletes the extension in the specified message.
<!-- {
  "blockType": "request",
  "name": "delete_opentypeextension"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions('Com.Contoso.Referral')
```

The second example deletes an extension in the specified group event.

```http
DELETE https://graph.microsoft.com/beta/groups('f5480dfd-7d77-4d0b-ba2e-3391953cc74a')/events('AAMkADVlN17IsAAA=')/extensions('Com.Contoso.Referral')
```

 

##### Response
Here is an example of the response.
<!-- {
  "blockType": "response",
  "truncated": false
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete opentypeextension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->