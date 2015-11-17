# openTypeExtension resource type

An OData v4 open type which allows you to specify custom data in instances of supported resources at runtime. 

### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.opentypeextension"
}-->

```json
{
  "extensionName": "String-value",
  "id": "String-value (identifier)"
}

```
### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|extensionName|String|A unique text identifier for an open type data extension. Required.|
|id|String| A fully qualified identifier that concatenates the extension type with the **extensionName**. Read-only.|

### Relationships
None


### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Create](../api/opentypeextension_create.md) | [openTypeExtension](opentypeextension.md), or [message](../resources/message.md), [event](../resources/event.md), or [contact](../resources/contact.md) that contains an openTypeExtension object. | Create an openTypeExtension object in an existing or new resource instance.| 
|[Get](../api/opentypeextension_get.md) | [openTypeExtension](opentypeextension.md) |Read properties and relationships of openTypeExtension object.|
|[Update](../api/opentypeextension_update.md) | [openTypeExtension](opentypeextension.md)	|Update openTypeExtension object. |
|[Delete](../api/opentypeextension_delete.md) | None |Delete openTypeExtension object. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "openTypeExtension resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->