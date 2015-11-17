# ChartFill: SetSolidColor

**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._

Sets the fill formatting of a chart element to a uniform color.
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/<id|name>/charts/<name>/format/fill/SetSolidColor
POST /workbook/worksheets/<id|name>/charts/<name>/title/format/fill/SetSolidColor
POST /workbook/worksheets/<id|name>/charts/<name>/legend/format/fill/SetSolidColor

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
|color|string|HTML color code representing the color of the border line, of the form #RRGGBB (e.g. "FFA500") or as a named HTML color (e.g. "orange").|

### Response
If successful, this method returns `, ` response code and [void](../resources/void.md) object in the response body.

### Example
Here is an example of how to call this API.
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "chartfill_setsolidcolor"
}-->
```http
POST https://graph.microsoft.com/beta/workbook/worksheets/<id|name>/charts/<name>/format/fill/SetSolidColor
Content-type: application/json
Content-length: 28

{
  "color": "color-value"
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
  "description": "ChartFill: SetSolidColor",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->