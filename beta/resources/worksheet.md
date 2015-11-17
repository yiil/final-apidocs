# Worksheet resource type
**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._
An Excel worksheet is a grid of cells. It can contain data, tables, charts, etc.

### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.worksheet"
}-->

```json
{
  "id": "string-value",
  "name": "string-value",
  "position": 1024,
  "visibility": "string-value"
}

```
### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|id|string|Returns a value that uniquely identifies the worksheet in a given workbook. The value of the identifier remains the same even when the worksheet is renamed or moved. Read-only.|
|name|string|The display name of the worksheet.|
|position|int|The zero-based position of the worksheet within the workbook.|
|visibility|string|The Visibility of the worksheet, Possible values are: `Visible`, `Hidden`, `VeryHidden`. Read-only.|

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|charts|[Chart](chart.md) collection|Returns collection of charts that are part of the worksheet. Read-only.|
|tables|[Table](table.md) collection|Collection of tables that are part of the worksheet. Read-only.|

### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get Worksheet](../api/worksheet_get.md) | [Worksheet](worksheet.md) |Read properties and relationships of worksheet object.|
|[Create Chart](../api/worksheet_post_charts.md) |[Chart](chart.md)| Create a new Chart by posting to the charts collection.|
|[List charts](../api/worksheet_list_charts.md) |[Chart](chart.md) collection| Get a Chart object collection.|
|[Create Table](../api/worksheet_post_tables.md) |[Table](table.md)| Create a new Table by posting to the tables collection.|
|[List tables](../api/worksheet_list_tables.md) |[Table](table.md) collection| Get a Table object collection.|
|[Update](../api/worksheet_update.md) | [Worksheet](worksheet.md)	|Update Worksheet object. |
|[Delete](../api/worksheet_delete.md) | None |Delete Worksheet object. |
|[Cell](../api/worksheet_cell.md)|[Range](range.md)|Gets the range object containing the single cell based on row and column numbers. The cell can be outside the bounds of its parent range, so long as it's stays within the worksheet grid.|
|[Delete](../api/worksheet_delete.md)|[void](void.md)|Deletes the worksheet from the workbook.|
|[Range](../api/worksheet_range.md)|[Range](range.md)|Gets the range object specified by the address or name.|
|[UsedRange](../api/worksheet_usedrange.md)|[Range](range.md)|The used range is the smallest range than encompasses any cells that have a value or formatting assigned to them. If the worksheet is blank, this function will return the top left cell.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Worksheet resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->