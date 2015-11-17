# Update chartdatalabels

**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._

Update the properties of chartdatalabels object.
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/worksheets/<id|name>/charts/<name>/datalabels
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
|position|string|DataLabelPosition value that represents the position of the data label. Possible values are: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.|
|separator|string|String representing the separator used for the data labels on a chart.|
|showBubbleSize|bool|Boolean value representing if the data label bubble size is visible or not.|
|showCategoryName|bool|Boolean value representing if the data label category name is visible or not.|
|showLegendKey|bool|Boolean value representing if the data label legend key is visible or not.|
|showPercentage|bool|Boolean value representing if the data label percentage is visible or not.|
|showSeriesName|bool|Boolean value representing if the data label series name is visible or not.|
|showValue|bool|Boolean value representing if the data label value is visible or not.|

### Response
If successful, this method returns a `200 OK` response code and updated [ChartDataLabels](../resources/chartdatalabels.md) object in the response body.
### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "update_chartdatalabels"
}-->
```http
PATCH https://graph.microsoft.com/beta/workbook/worksheets/<id|name>/charts/<name>/datalabels
Content-type: application/json
Content-length: 220

{
  "position": "position-value",
  "showValue": true,
  "showSeriesName": true,
  "showCategoryName": true,
  "showLegendKey": true,
  "showPercentage": true,
  "showBubbleSize": true,
  "separator": "separator-value"
}
```
##### Response
Here is an example of the response.
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.chartdatalabels"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 220

{
  "position": "position-value",
  "showValue": true,
  "showSeriesName": true,
  "showCategoryName": true,
  "showLegendKey": true,
  "showPercentage": true,
  "showBubbleSize": true,
  "separator": "separator-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update chartdatalabels",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->