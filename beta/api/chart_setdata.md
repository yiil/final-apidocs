# Chart: SetData

**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._

Resets the source data for the chart.
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/<id|name>/charts/<name>/SetData

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
|sourceData|Range or string|The address or name of the range that contains the source data. If an address or a worksheet-scoped name is used, it must include the worksheet name (e.g. "Sheet1!A5:B9"). |
|seriesBy|string|Optional. Specifies the way columns or rows are used as data series on the chart. Can be one of the following: Auto (default), Rows, Columns.  Possible values are: Auto`, `Columns`, `Rows`.|

### Response
If successful, this method returns `, ` response code and [void](../resources/void.md) object in the response body.

### Example
Here is an example of how to call this API.
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "chart_setdata"
}-->
```http
POST https://graph.microsoft.com/beta/workbook/worksheets/<id|name>/charts/<name>/SetData
Content-type: application/json
Content-length: 57

{
  "sourceData": {
  },
  "seriesBy": "seriesBy-value"
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
  "description": "Chart: SetData",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->