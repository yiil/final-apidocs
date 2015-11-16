# photo resource type



### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.photo"
}-->

```json
{
  "cameraMake": "string",
  "cameraModel": "string",
  "exposureDenominator": 1024,
  "exposureNumerator": 1024,
  "fNumber": 1024,
  "focalLength": 1024,
  "iso": 1024,
  "takenDateTime": {"@odata.type": "microsoft.graph.dateTimeOffset"}
}

```
### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|

### Relationships
None


### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get photo](../api/photo_get.md) | [photo](photo.md) |Read properties and relationships of photo object.|
|[Update](../api/photo_update.md) | [photo](photo.md)	|Update photo object. |
|[Delete](../api/photo_delete.md) | None |Delete photo object. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "photo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->