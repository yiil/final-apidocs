# Workbook resource type
**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._
Workbook is the top level object which contains related workbook objects such as worksheets, tables, ranges, etc.

### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbook"
}-->

```json
{
}

```
### Properties
None

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|names|[NamedItem](nameditem.md) collection|Represents a collection of workbook scoped named items (named ranges and constants). Read-only.|
|tables|[Table](table.md) collection|Represents a collection of tables associated with the workbook. Read-only.|
|worksheets|[Worksheet](worksheet.md) collection|Represents a collection of worksheets associated with the workbook. Read-only.|

### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[List names](../api/workbook_list_names.md) |[NamedItem](nameditem.md) collection| Get a NamedItem object collection.|
|[Create Table](../api/workbook_post_tables.md) |[Table](table.md)| Create a new Table by posting to the tables collection.|
|[List tables](../api/workbook_list_tables.md) |[Table](table.md) collection| Get a Table object collection.|
|[Create Worksheet](../api/workbook_post_worksheets.md) |[Worksheet](worksheet.md)| Create a new Worksheet by posting to the worksheets collection.|
|[List worksheets](../api/workbook_list_worksheets.md) |[Worksheet](worksheet.md) collection| Get a Worksheet object collection.|
|[Delete](../api/workbook_delete.md) | None |Delete Workbook object. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Workbook resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->