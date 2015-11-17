# NamedItem resource type
**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._
Represents a defined name for a range of cells or value. Names can be primitive named objects (as seen in the type below), range object, reference to a range. This object can be used to obtain range object associated with names.

### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.nameditem"
}-->

```json
{
  "name": "string-value",
  "type": "string-value",
  "value": {
    "@odata.type": "microsoft.graph.object"
  },
  "visible": true
}

```
### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|name|string|The name of the object. Read-only.|
|type|string|Indicates what type of reference is associated with the name. Possible values are: `String`, `Integer`, `Double`, `Boolean`, `Range`. Read-only.|
|value|[object](object.md)|Represents the formula that the name is defined to refer to. E.g. =Sheet14!$B$2:$H$12, =4.75, etc. Read-only.|
|visible|[bool](bool.md)|Specifies whether the object is visible or not.|

### Relationships
None


### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get NamedItem](../api/nameditem_get.md) | [NamedItem](nameditem.md) |Read properties and relationships of namedItem object.|
|[Update](../api/nameditem_update.md) | [NamedItem](nameditem.md)	|Update NamedItem object. |
|[Delete](../api/nameditem_delete.md) | None |Delete NamedItem object. |
|[Range](../api/nameditem_range.md)|[Range](range.md)|Returns the range object that is associated with the name. Throws an exception if the named item's type is not a range.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "NamedItem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->