# ChartLineFormat resource type
**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._
Enapsulates the formatting options for line elements.

### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartlineformat"
}-->

```json
{
  "color": "string-value"
}

```
### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|color|string|HTML color code representing the color of lines in the chart.|

### Relationships
None


### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get ChartLineFormat](../api/chartlineformat_get.md) | [ChartLineFormat](chartlineformat.md) |Read properties and relationships of chartLineFormat object.|
|[Update](../api/chartlineformat_update.md) | [ChartLineFormat](chartlineformat.md)	|Update ChartLineFormat object. |
|[Delete](../api/chartlineformat_delete.md) | None |Delete ChartLineFormat object. |
|[Clear](../api/chartlineformat_clear.md)|[void](void.md)|Clear the line format of a chart element.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartLineFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->