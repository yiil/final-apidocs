# ChartAxes resource type

**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._
Represents the chart axes.

### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.chartaxes"
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
|categoryAxis|[ChartAxis](chartaxis.md)|Represents the category axis in a chart. Read-only.|
|seriesAxis|[ChartAxis](chartaxis.md)|Represents the series axis of a 3-dimensional chart. Read-only.|
|valueAxis|[ChartAxis](chartaxis.md)|Represents the value axis in an axis. Read-only.|

### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Delete](../api/chartaxes_delete.md) | None |Delete ChartAxes object. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartAxes resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->