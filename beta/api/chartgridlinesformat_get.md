# Get ChartGridlinesFormat

**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._

Retrieve the properties and relationships of chartgridlinesformat object.
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/<id|name>/charts/<name>/axes/valueaxis/minorgridlines/format
GET /workbook/worksheets/<id|name>/charts/<name>/axes/valueaxis/majorgridlines/format
GET /workbook/worksheets/<id|name>/charts/<name>/axes/seriesaxis/majorgridlines/format
```
### Optional query parameters
This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.

### Request headers
| Name       | Type | Description|
|:-----------|:------|:----------|
| Authorization  |string | Bearer <token>. Required.| 
| Workbook-Session-Id  |string |It is recommended to include the workbook session Id along with the request. Optional.|

### Request body
Do not supply a request body for this method.
### Response
If successful, this method returns a `200 OK` response code and [ChartGridlinesFormat](../resources/chartgridlinesformat.md) object in the response body.
### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "get_chartgridlinesformat"
}-->
```http
GET https://graph.microsoft.com/beta/workbook/worksheets/<id|name>/charts/<name>/axes/valueaxis/minorgridlines/format
```
##### Response
Here is an example of the response.
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.chartgridlinesformat"
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
  "description": "Get ChartGridlinesFormat",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->