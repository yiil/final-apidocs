# Delete calendar

Delete a calendar.
### Prerequisites
One of the following **scopes** is required to execute this API: 
*Calendars.ReadWrite*
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/calendar
DELETE /users/<id>/calendar
DELETE /users/<userPrincipalName>/calendar
DELETE /me/calendars/<id>
DELETE /users/<id>/calendars/<id>
DELETE /users/<userPrincipalName>/calendars/<id>
DELETE /me/calendarGroup/calendars/<id>
DELETE /users/<id>/calendarGroup/calendars/<id>
DELETE /users/<userPrincipalName>/calendarGroup/calendars/<id>
DELETE /me/calendarGroups/<id>/calendars/<id>
DELETE /users/<id>/calendarGroups/<id>/calendars/<id>
DELETE /users/<userPrincipalName>/calendarGroups/<id>/calendars/<id>
DELETE /groups/<objectId>/calendar


```
### Request headers
| Name           |  Type    | Description|
|:---------------|:---------|:----------|
| Authorization  |  string  | Bearer <token>. Required. |

### Request body
Do not supply a request body for this method.


### Response
If successful, this method returns `204, No Content` response code. It does not return anything in the response body.

### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "delete_calendar"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/calendar
```
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
Status code: 204
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete calendar",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
