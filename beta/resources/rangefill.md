# RangeFill resource type
**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._
Represents the background of a range object.

### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.rangefill"
}-->

```json
{
  "color": "string-value"
}

```
### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|color|string|HTML color code representing the color of the border line, of the form #RRGGBB (e.g. "FFA500") or as a named HTML color (e.g. "orange")|

### Relationships
None


### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get RangeFill](../api/rangefill_get.md) | [RangeFill](rangefill.md) |Read properties and relationships of rangeFill object.|
|[Update](../api/rangefill_update.md) | [RangeFill](rangefill.md)	|Update RangeFill object. |
|[Delete](../api/rangefill_delete.md) | None |Delete RangeFill object. |
|[Clear](../api/rangefill_clear.md)|[void](void.md)|Resets the range background.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "RangeFill resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->