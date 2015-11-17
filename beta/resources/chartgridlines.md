# ChartGridlines resource type
**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._
Represents major or minor gridlines on a chart axis.

### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartgridlines"
}-->

```json
{
  "visible": true
}

```
### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|visible|[bool](bool.md)|Boolean value representing if the axis gridlines are visible or not.|

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|format|[ChartGridlinesFormat](chartgridlinesformat.md)|Represents the formatting of chart gridlines. Read-only.|

### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get ChartGridlines](../api/chartgridlines_get.md) | [ChartGridlines](chartgridlines.md) |Read properties and relationships of chartGridlines object.|
|[Update](../api/chartgridlines_update.md) | [ChartGridlines](chartgridlines.md)	|Update ChartGridlines object. |
|[Delete](../api/chartgridlines_delete.md) | None |Delete ChartGridlines object. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartGridlines resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->