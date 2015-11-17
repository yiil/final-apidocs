# ChartDataLabelFormat resource type
**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._
Encapsulates the format properties for the chart data labels.

### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartdatalabelformat"
}-->

```json
{
}

```
### Properties
None

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|fill|[ChartFill](chartfill.md)|Represents the fill format of the current chart data label. Read-only.|
|font|[ChartFont](chartfont.md)|Represents the font attributes (font name, font size, color, etc.) for a chart data label. Read-only.|

### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Delete](../api/chartdatalabelformat_delete.md) | None |Delete ChartDataLabelFormat object. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartDataLabelFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->