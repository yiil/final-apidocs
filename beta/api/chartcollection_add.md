# ChartCollection: Add

**Note:** _The Excel REST API reference is being made available to provide a preview to the upcoming release. These APIs are not yet released. We look forward to making them available as part of the Microsoft Graph /beta API set._

Creates a new chart.
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/worksheets/<id|name>/charts/Add

```
### Request headers
| Name       | Type | Description|
|:---------------|:--------|:----------|
| Authorization  |string | Bearer <token>. Required.| 
| Workbook-Session-Id  |string |It is recommended to include the workbook session Id along with the request. Optional.|

### Request body
In the request body, provide a JSON object with the following parameters.

| Parameter	   | Type	|Description|
|:---------------|:--------|:----------|
|type|string|Represents the type of a chart.  Possible values are: ColumnClustered`, `ColumnStacked`, `ColumnStacked100`, `BarClustered`, `BarStacked`, `BarStacked100`, `LineStacked`, `LineStacked100`, `LineMarkers`, `LineMarkersStacked`, `LineMarkersStacked100`, `PieOfPie`, `etc.`.|
|sourceData|Range|The range object that contains the source data.|
|seriesBy|string|Optional. Specifies the way columns or rows are used as data series on the chart.  Possible values are: Auto`, `Columns`, `Rows`.|

### Response
If successful, this method returns `, ` response code and [Chart](../resources/chart.md) object in the response body.

### Example
Here is an example of how to call this API.
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "chartcollection_add"
}-->
```http
POST https://graph.microsoft.com/beta/workbook/worksheets/<id|name>/charts/Add
Content-type: application/json
Content-length: 8673

{
  "type": "type-value",
  "sourceData": {
    "address": "address-value",
    "addressLocal": "addressLocal-value",
    "cellCount": 99,
    "columnCount": 99,
    "columnIndex": 99,
    "valueTypes": "valueTypes-value",
    "format": {
      "fill": {
        "color": "color-value"
      },
      "borders": [
        {
          "color": "color-value",
          "style": "style-value",
          "sideIndex": "sideIndex-value",
          "weight": "weight-value"
        }
      ],
      "font": {
        "bold": true,
        "color": "color-value",
        "italic": true,
        "name": "name-value",
        "size": 99,
        "underline": "underline-value"
      },
      "horizontalAlignment": "horizontalAlignment-value",
      "verticalAlignment": "verticalAlignment-value",
      "wrapText": true
    },
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
    },
    "worksheet": {
      "charts": [
        {
          "axes": {
            "categoryAxis": {
              "format": {
                "font": {
                  "bold": true,
                  "color": "color-value",
                  "italic": true,
                  "name": "name-value",
                  "size": 99,
                  "underline": "underline-value"
                },
                "line": {
                  "color": "color-value"
                }
              },
              "majorGridlines": {
                "visible": true,
                "format": {
                  "line": {
                    "color": "color-value"
                  }
                }
              },
              "majorUnit": {
              },
              "maximum": {
              },
              "minimum": {
              },
              "minorGridlines": {
                "visible": true,
                "format": {
                  "line": {
                    "color": "color-value"
                  }
                }
              },
              "minorUnit": {
              },
              "title": {
                "format": {
                  "font": {
                    "bold": true,
                    "color": "color-value",
                    "italic": true,
                    "name": "name-value",
                    "size": 99,
                    "underline": "underline-value"
                  }
                },
                "text": "text-value",
                "visible": true
              }
            },
            "seriesAxis": {
              "format": {
                "font": {
                  "bold": true,
                  "color": "color-value",
                  "italic": true,
                  "name": "name-value",
                  "size": 99,
                  "underline": "underline-value"
                },
                "line": {
                  "color": "color-value"
                }
              },
              "majorGridlines": {
                "visible": true,
                "format": {
                  "line": {
                    "color": "color-value"
                  }
                }
              },
              "majorUnit": {
              },
              "maximum": {
              },
              "minimum": {
              },
              "minorGridlines": {
                "visible": true,
                "format": {
                  "line": {
                    "color": "color-value"
                  }
                }
              },
              "minorUnit": {
              },
              "title": {
                "format": {
                  "font": {
                    "bold": true,
                    "color": "color-value",
                    "italic": true,
                    "name": "name-value",
                    "size": 99,
                    "underline": "underline-value"
                  }
                },
                "text": "text-value",
                "visible": true
              }
            },
            "valueAxis": {
              "format": {
                "font": {
                  "bold": true,
                  "color": "color-value",
                  "italic": true,
                  "name": "name-value",
                  "size": 99,
                  "underline": "underline-value"
                },
                "line": {
                  "color": "color-value"
                }
              },
              "majorGridlines": {
                "visible": true,
                "format": {
                  "line": {
                    "color": "color-value"
                  }
                }
              },
              "majorUnit": {
              },
              "maximum": {
              },
              "minimum": {
              },
              "minorGridlines": {
                "visible": true,
                "format": {
                  "line": {
                    "color": "color-value"
                  }
                }
              },
              "minorUnit": {
              },
              "title": {
                "format": {
                  "font": {
                    "bold": true,
                    "color": "color-value",
                    "italic": true,
                    "name": "name-value",
                    "size": 99,
                    "underline": "underline-value"
                  }
                },
                "text": "text-value",
                "visible": true
              }
            }
          },
          "dataLabels": {
            "format": {
              "font": {
                "bold": true,
                "color": "color-value",
                "italic": true,
                "name": "name-value",
                "size": 99,
                "underline": "underline-value"
              },
              "fill": {
              }
            },
            "position": "position-value",
            "showValue": true,
            "showSeriesName": true,
            "showCategoryName": true,
            "showLegendKey": true,
            "showPercentage": true,
            "showBubbleSize": true,
            "separator": "separator-value"
          },
          "height": 99,
          "left": 99,
          "legend": {
            "format": {
              "font": {
                "bold": true,
                "color": "color-value",
                "italic": true,
                "name": "name-value",
                "size": 99,
                "underline": "underline-value"
              },
              "fill": {
              }
            },
            "visible": true,
            "position": "position-value",
            "overlay": true
          },
          "name": "name-value",
          "series": [
            {
              "format": {
                "fill": {
                },
                "line": {
                  "color": "color-value"
                }
              },
              "name": "name-value",
              "points": [
                {
                }
              ]
            }
          ],
          "title": {
            "format": {
              "font": {
                "bold": true,
                "color": "color-value",
                "italic": true,
                "name": "name-value",
                "size": 99,
                "underline": "underline-value"
              },
              "fill": {
              }
            },
            "overlay": true,
            "text": "text-value",
            "visible": true
          },
          "top": 99,
          "width": 99,
          "format": {
            "fill": {
            },
            "font": {
              "bold": true,
              "color": "color-value",
              "italic": true,
              "name": "name-value",
              "size": 99,
              "underline": "underline-value"
            }
          }
        }
      ],
      "id": "id-value",
      "position": 99,
      "name": "name-value",
      "tables": [
        {
          "id": 99,
          "name": "name-value",
          "showHeaders": true,
          "showTotals": true,
          "style": "style-value",
          "columns": [
            {
              "id": 99,
              "name": "name-value",
              "index": 99,
              "values": {
              }
            }
          ],
          "rows": [
            {
              "index": 99,
              "values": {
              }
            }
          ]
        }
      ],
      "visibility": "visibility-value"
    }
  },
  "seriesBy": "seriesBy-value"
}
```

##### Response
Here is an example of the response.
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.chart"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 84

{
  "height": 99,
  "left": 99,
  "name": "name-value",
  "top": 99,
  "width": 99
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ChartCollection: Add",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->