# itemBody resource type

The body content of a message or event.

### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.itembody"
}-->

```json
{
  "content": "string",
  "contentType": {"@odata.type": "microsoft.graph.bodyType"}
}

```
### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|content|String|The content of the message or event.|
|contentType|String|The type of the content. Possible values are `Text` and `HTML`.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "itemBody resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->