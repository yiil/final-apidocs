# share resource type


### Methods

| Method       | Return Type  |Description|
|:---------------|:--------|:----------|
|[Get share](../api/share_get.md) | [share](share.md) |Read properties and relationships of share object.|
|[Create driveItem](../api/share_post_items.md) |[driveItem](driveitem.md)| Create a new driveItem by posting to the items collection.|
|[List items](../api/share_list_items.md) |[driveItem](driveitem.md) collection| Get a driveItem object collection.|
|[Update](../api/share_update.md) | [share](share.md) |Update share object. |
|[Delete](../api/share_delete.md) | None |Delete share object. |


### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|id|string| Read-only.|
|name|string||
|owner|[identitySet](identityset.md)||

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|items|[driveItem](driveitem.md) collection| Read-only. Nullable.|

### JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.share"
}-->

```json
{
  "id": "string (identifier)",
  "name": "string",
  "owner": {"@odata.type": "microsoft.graph.identitySet"}
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "share resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->