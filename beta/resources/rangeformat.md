# RangeFormat resource type
**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._
A format object encapsulating the range's font, fill, borders, alignment, and other properties.

### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.rangeformat"
}-->

```json
{
  "horizontalAlignment": "string-value",
  "verticalAlignment": "string-value",
  "wrapText": true
}

```
### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|horizontalAlignment|string|Represents the horizontal alignment for the specified object. Possible values are: `General`, `Left`, `Center`, `Right`, `Fill`, `Justify`, `CenterAcrossSelection`, `Distributed`.|
|verticalAlignment|string|Represents the vertical alignment for the specified object. Possible values are: `Top`, `Center`, `Bottom`, `Justify`, `Distributed`.|
|wrapText|[bool](bool.md)|Indicates if Excel wraps the text in the object. A null value indicates that the entire range doesn't have uniform wrap setting|

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|borders|[RangeBorder](rangeborder.md) collection|Collection of border objects that apply to the overall range selected Read-only.|
|fill|[RangeFill](rangefill.md)|Returns the fill object defined on the overall range. Read-only.|
|font|[RangeFont](rangefont.md)|Returns the font object defined on the overall range selected Read-only.|

### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get RangeFormat](../api/rangeformat_get.md) | [RangeFormat](rangeformat.md) |Read properties and relationships of rangeFormat object.|
|[Create RangeBorder](../api/rangeformat_post_borders.md) |[RangeBorder](rangeborder.md)| Create a new RangeBorder by posting to the borders collection.|
|[List borders](../api/rangeformat_list_borders.md) |[RangeBorder](rangeborder.md) collection| Get a RangeBorder object collection.|
|[Update](../api/rangeformat_update.md) | [RangeFormat](rangeformat.md)	|Update RangeFormat object. |
|[Delete](../api/rangeformat_delete.md) | None |Delete RangeFormat object. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "RangeFormat resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->