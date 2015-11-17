# ChartAxisTitle resource type

**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._
Represents the title of a chart axis.

### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartaxistitle"
}-->

```json
{
  "text": "string-value",
  "visible": true
}

```
### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|text|string|Represents the axis title.|
|visible|[bool](bool.md)|A boolean that specifies the visibility of an axis title.|

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|format|[ChartAxisTitleFormat](chartaxistitleformat.md)|Represents the formatting of chart axis title. Read-only.|

### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get ChartAxisTitle](../api/chartaxistitle_get.md) | [ChartAxisTitle](chartaxistitle.md) |Read properties and relationships of chartAxisTitle object.|
|[Update](../api/chartaxistitle_update.md) | [ChartAxisTitle](chartaxistitle.md)	|Update ChartAxisTitle object. |
|[Delete](../api/chartaxistitle_delete.md) | None |Delete ChartAxisTitle object. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartAxisTitle resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->