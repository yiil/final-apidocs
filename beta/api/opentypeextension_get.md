# Get extension

Get an open type data extension from the specified instance of a resource. 

The resource can be a message, calendar event, or contact of the signed-in user's on Office 365 or
Outlook.com. Or, it can be an event for an Office 365 group.

You can get an extension returned in one of two ways:
- Get just the extension in the REST response. You can specify the extension by name or fully qualified name, and
the extension can be in a user's message, event, or contact, or a group event.
 
- Get the resource instance expanded with the extension in the REST response. To do this, 
use the `$expand` parameter, and specify a `$filter` on the **Id** property against the extension name
or fully qualified name. The extension can be in a user's message, event, or contact, but not 
in a group event. 


### Prerequisites

One of the following **scopes** is required to execute this API, depending on the resource you're
getting the extension from:

- _Mail.Read_
- _Calendars.Read_
- _Contacts.Read_
- _Group.Read.All_
 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
GET /me/messages/<id>/extensions/<eId>
GET /users/<objectId>/messages/<id>/extensions/<eId>
GET /me/messages/<id>?$expand=Extensions($filter=Id eq 'eId')
GET /users/<objectId>?$expand=Extensions($filter=Id eq 'eId')

GET /me/events/<id>/extensions/<eId>
GET /users/<objectId>/events/<id>/extensions/<eId>
GET /me/events/<id>?$expand=Extensions($filter=Id eq 'eId')
GET /users/<objectId>?$expand=Extensions($filter=Id eq 'eId')

GET /me/contacts/<id>/extensions/<eId>
GET /users/<objectId>/contacts/<id>/extensions/<eId>
GET /me/contacts/<id>?$expand=Extensions($filter=Id eq 'eId')
GET /users/<objectId>?$expand=Extensions($filter=Id eq 'eId')

GET /groups/<gId>/events/<id>/extensions/<eId>

```

### Parameters
|**Parameter**|**Type**|**Description**|
|:-----|:-----|:-----|
|_URL parameters_|
|id|string|A unique identifier for an instance of a resource (message, event, or contact). Required.|
|eId|string|This can be an extension name which is a unique text identifier for an extension, or a fully qualified name which concatenates the extension type and unique text identifier. The fully qualified name is returned in the `Id` property when you create the extension. Required.|
|objectId|string|A unique identifier for the signed-in user. Required.|
|gId|string|A unique group ID. Required.|


### Optional query parameters
|Name|Value|Description|
|:---------------|:--------|:-------|
|$expand|string|Get and expand a resource instance to include the specified extension. |


### Request headers
| Name       | Value |
|:---------------|:----------|
| Authorization | Bearer %token%|


### Request body
Do not supply a request body for this method.
### Response
If successful, this method returns a `200 OK` response code and [openTypeExtension](../resources/opentypeextension.md) object in the response body.
### Example
##### Request
The first example references an extension by its name and gets the extension in the specified message. 
<!-- {
  "blockType": "request",
  "name": "get_opentypeextension"
}-->
```http
GET https://graph.microsoft.com/beta/me/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions('Com.Contoso.Referral')
```

The second example references an extension by its ID (fully qualified name) and gets the extension in 
the same message as the first example.

```
GET https://graph.microsoft.com/beta/me/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions('Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral')
```

The third example references an extension by its name and gets the extension in the specified group event.

```
GET https://graph.microsoft.com/beta/groups('f5480dfd-7d77-4d0b-ba2e-3391953cc74a')/events('AAMkADVl17IsAAA=')/extensions('Com.Contoso.Deal') 
```

The fourth example gets and expands the specified message by including the extension returned from a filter. 
The filter returns the extension that has its `Id` matching a fully qualified name.

```
GET https://graph.microsoft.com/beta/me/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')?$expand=Extensions($filter=Id%20eq%20'Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral')
```


##### Response
Here is the response from the first two example requests.
<!-- {
  "blockType": "response",
  "truncated": false,
  "@odata.type": "microsoft.graph.opentypeextension"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

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

****

Here is the response from the third example request.

```
{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#groups('f5480dfd-7d77-4d0b-ba2e-3391953cc74a')/Events('AAMkADVl7IsAAA%3D')/Extensions/$entity",
    "@odata.type": "#Microsoft.Graph.OpenTypeExtension",
    "Id": "Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Deal",
    "ExtensionName": "Com.Contoso.Deal",
    "CompanyName": "Alpine Skis",
    "DealValue": 1010100,
    "ExpirationDate": "2015-07-03T13:04:00Z"
}
```

****

And here is the response from the fourth example request.

```
{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Me/Messages/$entity",
    "@odata.id": "https://graph.microsoft.com/beta/Users('ddfc984d-b826-40d7-b48b-57002df85e00@1717f226-49d1-4d0c-9d74-709fad6677b4')/Messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')",
    "@odata.etag": "W/\"CQAAABYAAACY4MQpaFz9SbqUDe4+bs88AABNsWMM\"",
    "Id": "AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===",
    "ChangeKey": "CQAAABYAAACY4MQpaFz9SbqUDe4+bs88AABNsWMM",
    "Categories": [
    ],
    "CreateDateTime": "2015-06-19T02:03:31Z",
    "LastModifiedDateTime": "2015-08-13T02:28:00Z",
    "Subject": "Attached is the requested info",
    "BodyPreview": "See the images attached.",
    "Body": {
        "ContentType": "HTML",
        "Content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r\n<style type=\"text/css\" style=\"display:none;\"><!-- P {margin-top:0;margin-bottom:0;} --></style>\r\n</head>\r\n<body dir=\"ltr\">\r\n<div id=\"divtagdefaultwrapper\" style=\"font-size:12pt;color:#000000;background-color:#FFFFFF;font-family:Calibri,Arial,Helvetica,sans-serif;\">\r\n<p>See the images attached. <br>\r\n</p>\r\n</div>\r\n</body>\r\n</html>\r\n"
    },
    "Importance": "Normal",
    "HasAttachments": true,
    "ParentFolderId": "AQMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===QAAAA==",
    "From": {
        "EmailAddress": {
            "Address": "desmond@contoso.com",
            "Name": "Desmond Raley"
        }
    },
    "Sender": {
        "EmailAddress": {
            "Address": "desmond@contoso.com",
            "Name": "Desmond Raley"
        }
    },
    "ToRecipients": [
        {
            "EmailAddress": {
                "Address": "wendy@contoso.com",
                "Name": "Wendy Molina"
            }
        }
    ],
    "CcRecipients": [
    ],
    "BccRecipients": [
    ],
    "ReplyTo": [
    ],
    "ConversationId": "AAQkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===mivdTmQ=",
    "ReceivedDateTime": "2015-06-19T02:05:04Z",
    "SentDateTime": "2015-06-19T02:04:59Z",
    "IsDeliveryReceiptRequested": false,
    "IsReadReceiptRequested": false,
    "IsDraft": false,
    "IsRead": true,
    "WebLink": "https://outlook.office.com/owa/?ItemID=AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===%2FNJTqt5NqHlVnKVBwCY4MQpaFz9SbqUDe4%2Bbs88AAAAAAEJAACY4MQpaFz9SbqUDe4%2Bbs88AAApA4JMAAA%3D&exvsurl=1&viewmodel=ReadMessageItem",
    "MentionedMe": null,
    "Mentioned": [
    ],
    "InferenceClassification": "Focused",
    "Extensions@odata.context": "https://graph.microsoft.com/beta/$metadata#Users('desmond40contoso.com')/Messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/Extensions", 
    "Extensions": [ 
      { 
        "@odata.type": "#Microsoft.Graph.OpenTypeExtension",
        "@odata.id": "https://graph.microsoft.com/beta/Users('ddfc984d-b826-40d7-b48b-57002df85e00@1717f226-49d1-4d0c-9d74-709fad6677b4')/Messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions('Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral')",
        "ExtensionName": "Com.Contoso.Referral",
        "Id": "Microsoft.OutlookServices.OpenTypeExtension.Com.Contoso.Referral",
        "CompanyName": "Wingtip Toys",
        "DealValue": 500050,
        "ExpirationDate": "2015-12-03T10:00:00Z"
      }
     ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get openTypeExtension",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->