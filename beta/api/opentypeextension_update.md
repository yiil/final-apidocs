# Update extension

Update an open type data extension with the properties in the request body:
- If a property in the request body matches the name of an existing property in the extension, the data in the 
extension is updated.
- Otherwise that property and its data are added to the extension. 

The extension can be in a message, event, or contact in the signed-in user's mailbox on Office 365 or
Outlook.com. 


### Prerequisites

One of the following **scopes** is required to execute this API, depending on the resource you're
creating the extension in:

- _Mail.ReadWrite_
- _Calendars.ReadWrite_
- _Contacts.ReadWrite_
 
### HTTP request
<!-- { "blockType": "ignored" } -->

```http
PATCH /me/messages/<id>/extensions/<eId>
PATCH /users/<objectId>/messages/<id>/extensions/<eId>

PATCH /me/events/<id>/extensions/<eId>
PATCH /users/<objectId>/events/<id>/extensions/<eId>

PATCH /me/contacts/<id>/extensions/<eId>
PATCH /users/<objectId>/contacts/<id>/extensions/<eId>
```


### Parameters
|**Parameter**|**Type**|**Description**|
|:-----|:-----|:-----|
|_URL parameters_|
|id|string|A unique identifier for an instance of a resource (message, event, or contact). Required.|
|eId|string|This can be an extension name which is a unique text identifier for an extension, or a fully qualified name which concatenates the extension type and unique text identifier. The fully qualified name is returned in the `Id` property when you create the extension. Required.|
|objectId|string|A unique identifier for the signed-in user. Required.|


### Request headers
| Name       | Value |
|:---------------|:----------|
| Authorization | Bearer %token%|
| Content-Type | application/json |

### Request body

Provide a JSON body of an [openTypeExtension](../resources/openTypeExtension.md) object, with the 
following required name-value pairs, and any custom data to change or add to that extension:

| Name       | Value |
|:---------------|:----------|
| @odata.type | Microsoft.Graph.OpenTypeExtension |
| ExtensionName | %unique_string% |


### Response

If successful, this method returns a `200 Ok` response code and the updated
[openTypeExtension](../resources/openTypeExtension.md) object.


### Example
##### Request

<a name="originalExample"></a>

Each of the following 2 examples updates an extension represented by the following JSON payload:

```http
{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Me/Messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/Extensions/$entity",
    "@odata.type": "#Microsoft.Graph.OpenTypeExtension",
    "@odata.id": "https://graph.microsoft.com/beta/Users('ddfc984d-b826-40d7-b48b-57002df85e00@1717f226-49d1-4d0c-9d74-709fad6677b4')/Messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions
('Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral')",
    "ExtensionName": "Com.Contoso.Referral",
    "Id": "Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral",
    "CompanyName": "Wingtip Toys",
    "DealValue": 500050,
    "ExpirationDate": "2015-12-03T10:00:00Z"
}
```
 
The first example references the extension by its name:

```http
PATCH https://graph.microsoft.com/beta/me/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/Extensions('Com.Contoso.Referral')
```

The second example references the extension by its fully qualified name:

```http
PATCH https://graph.microsoft.com/beta/me/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/Extensions('Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral')
```

You can use either example request and the following request body to update the [original extension](#originalExample) by:
- Changing `CompanyName` from `Wingtip Toys` to `Wingtip Toys (USA)`
- Changing `DealValue` from `500050` to `500100`
- Adding new data as the custom property `Updated`

```http
{
    "@odata.type": "Microsoft.Graph.OpenTypeExtension",
    "ExtensionName": "Com.Contoso.Referral",
    "CompanyName": "Wingtip Toys (USA)",
    "DealValue": "500100",
    "ExpirationDate": "2015-12-03T10:00:00.000Z",
    "Updated": "2015-10-29T11:00:00.000Z"
} 
```

****



##### Response

Here is the response for either the first or second example request.

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Me/Messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/Extensions/$entity",
    "@odata.type": "#Microsoft.Graph.OpenTypeExtension",
    "@odata.id": "https://graph.microsoft.com/beta/Users('ddfc984d-b826-40d7-b48b-57002df85e00@1717f226-49d1-4d0c-9d74-709fad6677b4')/Messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions
('Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral')",
    "Id": "Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral",
    "ExtensionName": "Com.Contoso.Referral",
    "CompanyName": "Wingtip Toys (USA)",
    "DealValue": 500100,
    "ExpirationDate": "2015-12-03T10:00:00Z",
    "Updated": "2015-10-29T11:00:00.000Z"
}
```



<!-- This page was manually created. -->
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create extension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->