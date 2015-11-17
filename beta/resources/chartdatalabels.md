# ChartDataLabels resource type
**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._
Represents a collection of all the data labels on a chart point.

### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartdatalabels"
}-->

```json
{
  "position": "string-value",
  "separator": "string-value",
  "showBubbleSize": true,
  "showCategoryName": true,
  "showLegendKey": true,
  "showPercentage": true,
  "showSeriesName": true,
  "showValue": true
}

```
### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|position|string|DataLabelPosition value that represents the position of the data label. Possible values are: `None`, `Center`, `InsideEnd`, `InsideBase`, `OutsideEnd`, `Left`, `Right`, `Top`, `Bottom`, `BestFit`, `Callout`.|
|separator|string|String representing the separator used for the data labels on a chart.|
|showBubbleSize|[bool](bool.md)|Boolean value representing if the data label bubble size is visible or not.|
|showCategoryName|[bool](bool.md)|Boolean value representing if the data label category name is visible or not.|
|showLegendKey|[bool](bool.md)|Boolean value representing if the data label legend key is visible or not.|
|showPercentage|[bool](bool.md)|Boolean value representing if the data label percentage is visible or not.|
|showSeriesName|[bool](bool.md)|Boolean value representing if the data label series name is visible or not.|
|showValue|[bool](bool.md)|Boolean value representing if the data label value is visible or not.|

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|format|[ChartDataLabelFormat](chartdatalabelformat.md)|Represents the format of chart data labels, which includes fill and font formatting. Read-only.|

### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get ChartDataLabels](../api/chartdatalabels_get.md) | [ChartDataLabels](chartdatalabels.md) |Read properties and relationships of chartDataLabels object.|
|[Update](../api/chartdatalabels_update.md) | [ChartDataLabels](chartdatalabels.md)	|Update ChartDataLabels object. |
|[Delete](../api/chartdatalabels_delete.md) | None |Delete ChartDataLabels object. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartDataLabels resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->