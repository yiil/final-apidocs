# Range resource type
**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._
Range represents a set of one or more contiguous cells such as a cell, a row, a column, block of cells, etc.

### JSON representation

Here is a JSON representation of the resource

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.range"
}-->

```json
{
  "address": "string-value",
  "addressLocal": "string-value",
  "cellCount": 1024,
  "columnCount": 1024,
  "columnIndex": 1024,
  "formulas": {
    "@odata.type": "microsoft.graph.object"
  },
  "formulasLocal": {
    "@odata.type": "microsoft.graph.object"
  },
  "numberFormat": {
    "@odata.type": "microsoft.graph.object"
  },
  "rowCount": 1024,
  "rowIndex": 1024,
  "text": {
    "@odata.type": "microsoft.graph.object"
  },
  "valueTypes": "string-value",
  "values": {
    "@odata.type": "microsoft.graph.object"
  }
}

```
### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|address|string|Represents the range reference in A1-style. Address value will contain the Sheet reference (e.g. Sheet1!A1:B4). Read-only.|
|addressLocal|string|Represents range reference for the specified range in the language of the user. Read-only.|
|cellCount|int|Number of cells in the range. Read-only.|
|columnCount|int|Represents the total number of columns in the range. Read-only.|
|columnIndex|int|Represents the column number of the first cell in the range. Zero-indexed. Read-only.|
|formulas|[object](object.md)|Represents the formula in A1-style notation.|
|formulasLocal|[object](object.md)|Represents the formula in A1-style notation, in the user's language and number-formatting locale.  For example, the English "=SUM(A1, 1.5)" formula would become "=SUMME(A1; 1,5)" in German.|
|numberFormat|[object](object.md)|Represents Excel's number format code for the given cell.|
|rowCount|int|Returns the total number of rows in the range. Read-only.|
|rowIndex|int|Returns the row number of the first cell in the range. Zero-indexed. Read-only.|
|text|[object](object.md)|Text values of the specified range. The Text value will not depend on the cell width. The # sign substitution that happens in Excel UI will not affect the text value returned by the API. Read-only.|
|valueTypes|string|Represents the type of data of each cell. Possible values are: `Unknown`, `Empty`, `String`, `Integer`, `Double`, `Boolean`, `Error`. Read-only.|
|values|[object](object.md)|Represents the raw values of the specified range. The data returned could be of type string, number, or a boolean. Cell that contain an error will return the error string.|

### Relationships
| Relationship | Type	|Description|
|:---------------|:--------|:----------|
|format|[RangeFormat](rangeformat.md)|Returns a format object, encapsulating the range's font, fill, borders, alignment, and other properties. Read-only.|
|worksheet|[Worksheet](worksheet.md)|The worksheet containing the current range. Read-only.|

### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get Range](../api/range_get.md) | [Range](range.md) |Read properties and relationships of range object.|
|[Update](../api/range_update.md) | [Range](range.md)	|Update Range object. |
|[Delete](../api/range_delete.md) | None |Delete Range object. |
|[BoundingRect](../api/range_boundingrect.md)|[Range](range.md)|Gets the smallest range object that encompasses the given ranges. For example, the GetBoundingRect of "B2:C5" and "D10:E15" is "B2:E16".|
|[Cell](../api/range_cell.md)|[Range](range.md)|Gets the range object containing the single cell based on row and column numbers. The cell can be outside the bounds of its parent range, so long as it's stays within the worksheet grid. The returned cell is located relative to the top left cell of the range.|
|[Clear](../api/range_clear.md)|[void](void.md)|Clear range values, format, fill, border, etc.|
|[Column](../api/range_column.md)|[Range](range.md)|Gets a column contained in the range.|
|[Delete](../api/range_delete.md)|[void](void.md)|Deletes the cells associated with the range.|
|[EntireColumn](../api/range_entirecolumn.md)|[Range](range.md)|Gets an object that represents the entire column of the range.|
|[EntireRow](../api/range_entirerow.md)|[Range](range.md)|Gets an object that represents the entire row of the range.|
|[Insert](../api/range_insert.md)|[Range](range.md)|Inserts a cell or a range of cells into the worksheet in place of this range, and shifts the other cells to make space. Returns a new Range object at the now blank space.|
|[Intersection](../api/range_intersection.md)|[Range](range.md)|Gets the range object that represents the rectangular intersection of the given ranges.|
|[LastCell](../api/range_lastcell.md)|[Range](range.md)|Gets the last cell within the range. For example, the last cell of "B2:D5" is "D5".|
|[LastColumn](../api/range_lastcolumn.md)|[Range](range.md)|Gets the last column within the range. For example, the last column of "B2:D5" is "D2:D5".|
|[LastRow](../api/range_lastrow.md)|[Range](range.md)|Gets the last row within the range. For example, the last row of "B2:D5" is "B5:D5".|
|[OffsetRange](../api/range_offsetrange.md)|[Range](range.md)|Gets an object which represents a range that's offset from the specified range. The dimension of the returned range will match this range. If the resulting range is forced outside the bounds of the worksheet grid, an exception will be thrown.|
|[Row](../api/range_row.md)|[Range](range.md)|Gets a row contained in the range.|
|[Select](../api/range_select.md)|[void](void.md)|Selects the specified range in the Excel UI.|
|[UsedRange](../api/range_usedrange.md)|[Range](range.md)|Returns the used range of the given range object.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Range resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->