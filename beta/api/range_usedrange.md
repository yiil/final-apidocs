# Range: UsedRange

**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._

Returns the used range of the given range object.
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names/<name>/range/UsedRange
POST /workbook/bindings/<id>/range/UsedRange
POST /workbook/tables/<id|name>/range/UsedRange

```
### Request headers
| Name       | Type | Description|
|:---------------|:--------|:----------|
| Authorization  |string | Bearer <token>. Required.| 
| Workbook-Session-Id  |string |It is recommended to include the workbook session Id along with the request. Optional.|

### Request body

### Response
If successful, this method returns `, ` response code and [Range](../resources/range.md) object in the response body.

### Example
Here is an example of how to call this API.
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "range_usedrange"
}-->
```http
POST https://graph.microsoft.com/beta/workbook/names/<name>/range/UsedRange
```

##### Response
Here is an example of the response.
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.range"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 313

{
  "address": "address-value",
  "addressLocal": "addressLocal-value",
  "cellCount": 99,
  "columnCount": 99,
  "columnIndex": 99,
  "valueTypes": "valueTypes-value",
  "formulas": {
  },
  "formulasLocal": {
  },
  "numberFormat": {
  },
  "rowCount": 99,
  "rowIndex": 99,
  "text": {
  },
  "values": {
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Range: UsedRange",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->