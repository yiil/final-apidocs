# Create Table

**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._

Use this API to create a new Table.
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/tables

```
### Request headers
| Name       | Type | Description|
|:---------------|:--------|:----------|
| Authorization  |string | Bearer <token>. Required.| 
| Workbook-Session-Id  |string |It is recommended to include the workbook session Id along with the request. Optional.|

### Request body
In the request body, supply a JSON representation of [Table](../resources/table.md) object.


### Response
If successful, this method returns `201, Created` response code and [Table](../resources/table.md) object in the response body.

### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "create_table_from_workbook"
}-->
```http
POST https://graph.microsoft.com/beta/workbook
```
In the request body, supply a JSON representation of [Table](../resources/table.md) object.
##### Response
Here is an example of the response.
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.table"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 109

{
  "id": 99,
  "name": "name-value",
  "showHeaders": true,
  "showTotals": true,
  "style": "style-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Table",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->