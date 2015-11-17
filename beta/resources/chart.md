# Chart resource type

**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._
Represents a chart object in a workbook.

### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chart"
}-->

```json
{
  "height": 1024,
  "left": 1024,
  "name": "string-value",
  "top": 1024,
  "width": 1024
}

```
### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|height|double|Represents the height, in points, of the chart object.|
|left|double|The distance, in points, from the left side of the chart to the worksheet origin.|
|name|string|Represents the name of a chart object.|
|top|double|Represents the distance, in points, from the top edge of the object to the top of row 1 (on a worksheet) or the top of the chart area (on a chart).|
|width|double|Represents the width, in points, of the chart object.|

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|axes|[ChartAxes](chartaxes.md)|Represents chart axes. Read-only.|
|dataLabels|[ChartDataLabels](chartdatalabels.md)|Represents the datalabels on the chart. Read-only.|
|format|[ChartAreaFormat](chartareaformat.md)|Encapsulates the format properties for the chart area. Read-only.|
|legend|[ChartLegend](chartlegend.md)|Represents the legend for the chart. Read-only.|
|series|[ChartSeries](chartseries.md) collection|Represents either a single series or collection of series in the chart. Read-only.|
|title|[ChartTitle](charttitle.md)|Represents the title of the specified chart, including the text, visibility, position and formating of the title. Read-only.|

### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get Chart](../api/chart_get.md) | [Chart](chart.md) |Read properties and relationships of chart object.|
|[Create ChartSeries](../api/chart_post_series.md) |[ChartSeries](chartseries.md)| Create a new ChartSeries by posting to the series collection.|
|[List series](../api/chart_list_series.md) |[ChartSeries](chartseries.md) collection| Get a ChartSeries object collection.|
|[Update](../api/chart_update.md) | [Chart](chart.md)	|Update Chart object. |
|[Delete](../api/chart_delete.md) | None |Delete Chart object. |
|[Delete](../api/chart_delete.md)|[void](void.md)|Deletes the chart object.|
|[SetData](../api/chart_setdata.md)|[void](void.md)|Resets the source data for the chart.|
|[SetPosition](../api/chart_setposition.md)|[void](void.md)|Positions the chart relative to cells on the worksheet.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Chart resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->