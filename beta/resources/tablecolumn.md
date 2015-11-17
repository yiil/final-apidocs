# TableColumn resource type
**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._
Represents a column in a table.

### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.tablecolumn"
}-->

```json
{
  "id": 1024,
  "index": 1024,
  "name": "string-value",
  "values": {
    "@odata.type": "microsoft.graph.object"
  }
}

```
### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|id|int|Returns a unique key that identifies the column within the table. Read-only.|
|index|int|Returns the index number of the column within the columns collection of the table. Zero-indexed. Read-only.|
|name|string|Returns the name of the table column. Read-only.|
|values|[object](object.md)|Represents the raw values of the specified range. The data returned could be of type string, number, or a boolean. Cell that contain an error will return the error string.|

### Relationships
None


### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get TableColumn](../api/tablecolumn_get.md) | [TableColumn](tablecolumn.md) |Read properties and relationships of tableColumn object.|
|[Update](../api/tablecolumn_update.md) | [TableColumn](tablecolumn.md)	|Update TableColumn object. |
|[Delete](../api/tablecolumn_delete.md) | None |Delete TableColumn object. |
|[DataBodyRange](../api/tablecolumn_databodyrange.md)|[Range](range.md)|Gets the range object associated with the data body of the column.|
|[HeaderRowRange](../api/tablecolumn_headerrowrange.md)|[Range](range.md)|Gets the range object associated with the header row of the column.|
|[Range](../api/tablecolumn_range.md)|[Range](range.md)|Gets the range object associated with the entire column.|
|[TotalRowRange](../api/tablecolumn_totalrowrange.md)|[Range](range.md)|Gets the range object associated with the totals row of the column.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableColumn resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->