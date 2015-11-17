# Delete ChartLineFormat

**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._

Delete ChartLineFormat.
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
DELETE /workbook/worksheets/<id|name>/charts/<name>/axes/valueaxis/format/line
DELETE /workbook/worksheets/<id|name>/charts/<name>/axes/seriesaxis/format/line
DELETE /workbook/worksheets/<id|name>/charts/<name>/axes/categoryaxis/format/line

```
### Request headers
| Name       | Type | Description|
|:---------------|:--------|:----------|
| Authorization  |string | Bearer <token>. Required.| 
| Workbook-Session-Id  |string |It is recommended to include the workbook session Id along with the request. Optional.|

### Request body
Do not supply a request body for this method.


### Response
If successful, this method returns `204, No Content` response code. It does not return anything in the response body.

### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "delete_chartlineformat"
}-->
```http
DELETE https://graph.microsoft.com/beta/workbook/worksheets/<id|name>/charts/<name>/axes/valueaxis/format/line
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
  "description": "Delete ChartLineFormat",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->