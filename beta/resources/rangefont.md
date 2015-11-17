# RangeFont resource type
**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._
This object represents the font attributes (font name, font size, color, etc.) for an object.

### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.rangefont"
}-->

```json
{
  "bold": true,
  "color": "string-value",
  "italic": true,
  "name": "string-value",
  "size": 1024,
  "underline": "string-value"
}

```
### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|bold|[bool](bool.md)|Represents the bold status of font.|
|color|string|HTML color code representation of the text color. E.g. #FF0000 represents Red.|
|italic|[bool](bool.md)|Represents the italic status of the font.|
|name|string|Font name (e.g. "Calibri")|
|size|double|Font size.|
|underline|string|Type of underline applied to the font. Possible values are: `None`, `Single`, `Double`, `SingleAccountant`, `DoubleAccountant`.|

### Relationships
None


### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get RangeFont](../api/rangefont_get.md) | [RangeFont](rangefont.md) |Read properties and relationships of rangeFont object.|
|[Update](../api/rangefont_update.md) | [RangeFont](rangefont.md)	|Update RangeFont object. |
|[Delete](../api/rangefont_delete.md) | None |Delete RangeFont object. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "RangeFont resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->