# Chart: SetPosition

**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._

Positions the chart relative to cells on the worksheet.
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/<id|name>/charts/<name>/SetPosition

```
### Request headers
| Name       | Type | Description|
|:---------------|:--------|:----------|
| Authorization  |string | Bearer <token>. Required.| 
| Workbook-Session-Id  |string |It is recommended to include the workbook session Id along with the request. Optional.|

### Request body
In the request body, provide a JSON object with the following parameters.

| Parameter	   | Type	|Description|
|:---------------|:--------|:----------|
|startCell|Range or string|The start cell. This is where the chart will be moved to. The start cell is the top-left or top-right cell, depending on the user's right-to-left display settings.|
|endCell|Range or string|Optional. (Optional) The end cell. If specified, the chart's width and height will be set to fully cover up this cell/range.|

### Response
If successful, this method returns `, ` response code and [void](../resources/void.md) object in the response body.

### Example
Here is an example of how to call this API.
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "chart_setposition"
}-->
```http
POST https://graph.microsoft.com/beta/workbook/worksheets/<id|name>/charts/<name>/SetPosition
Content-type: application/json
Content-length: 44

{
  "startCell": {
  },
  "endCell": {
  }
}
```

##### Response
Here is an example of the response.
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.void"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 3

{
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Chart: SetPosition",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->