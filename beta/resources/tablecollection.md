# TableCollection resource type
**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._
Represents a collection of all the tables that are part of the workbook.

### Properties
None

### Relationships
None


### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[List](../api/table_list.md) | [Table](table.md) collection |Get table object collection. |
|[Delete](../api/tablecollection_delete.md) | None |Delete TableCollection object. |
|[Add](../api/tablecollection_add.md)|[Table](table.md)|Create a new table. The range source address determines the worksheet under which the table will be added. If the table cannot be added (e.g., because the address is invalid, or the table would overlap with another table), an error will be thrown.|


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "TableCollection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->