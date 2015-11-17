# Update chartgridlines

**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._

Update the properties of chartgridlines object.
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/<id|name>/charts/<name>/axes/valueaxis/minorgridlines
PATCH /workbook/worksheets/<id|name>/charts/<name>/axes/valueaxis/majorgridlines
PATCH /workbook/worksheets/<id|name>/charts/<name>/axes/seriesaxis/majorgridlines
```
### Optional request headers
| Name       | Type | Description|
|:-----------|:------|:----------|
| Authorization  |string | Bearer <token>. Required.| 
| Workbook-Session-Id  |string |It is recommended to include the workbook session Id along with the request. Optional.|

### Request body
In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.

| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|visible|bool|Boolean value representing if the axis gridlines are visible or not.|

### Response
If successful, this method returns a `200 OK` response code and updated [ChartGridlines](../resources/chartgridlines.md) object in the response body.
### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "update_chartgridlines"
}-->
```http
PATCH https://graph.microsoft.com/beta/workbook/worksheets/<id|name>/charts/<name>/axes/valueaxis/minorgridlines
Content-type: application/json
Content-length: 21

{
  "visible": true
}
```
##### Response
Here is an example of the response.
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.chartgridlines"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 21

{
  "visible": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update chartgridlines",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->