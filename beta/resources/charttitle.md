# ChartTitle resource type
**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._
Represents a chart title object of a chart.

### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.charttitle"
}-->

```json
{
  "overlay": true,
  "text": "string-value",
  "visible": true
}

```
### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|overlay|[bool](bool.md)|Boolean value representing if the chart title will overlay the chart or not.|
|text|string|Represents the title text of a chart.|
|visible|[bool](bool.md)|A boolean value the represents the visibility of a chart title object.|

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|format|[ChartTitleFormat](charttitleformat.md)|Represents the formatting of a chart title, which includes fill and font formatting. Read-only.|

### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get ChartTitle](../api/charttitle_get.md) | [ChartTitle](charttitle.md) |Read properties and relationships of chartTitle object.|
|[Update](../api/charttitle_update.md) | [ChartTitle](charttitle.md)	|Update ChartTitle object. |
|[Delete](../api/charttitle_delete.md) | None |Delete ChartTitle object. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartTitle resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->