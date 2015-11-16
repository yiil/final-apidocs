# checklistItemCollection resource type

The ChecklistItemCollection* resource represents the collection of checklist items on a task. It is part of the [task details](taskdetails.md) object. The value in the property-value pair is the [checklistItem](checklistitem.md) object.

*Note that this is an Open Type.

### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.checklistitemcollection"
}-->

```json
{
}

```
```json
{
}

```
### Properties
Properties of an Open Type can be defined by the client. In this case, the client should provide **GUIDs** as properties and their values must be [checklistItem](checklistitem.md) objects. Example is shown above. To remove an item in the checklist, set the value of the property to `null`.

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "checklistItemCollection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->