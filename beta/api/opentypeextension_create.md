# Create extension

Create an open type data extension in a new or existing instance of a resource. 

The resource can be a message, calendar event, or contact in the signed-in user's mailbox on Office 365 or
Outlook.com. Or, it can be an event for an Office 365 group.


### Prerequisites

One of the following **scopes** is required to execute this API, depending on the resource you're
creating the extension in:

- _Mail.ReadWrite_
- _Calendars.ReadWrite_
- _Contacts.ReadWrite_
- _Group.ReadWrite.All_
 
### HTTP request
<!-- { "blockType": "ignored" } -->

To create an extension in a new resource instance, use the same REST request as creating the
instance, and include the properties of the new resource instance _and of the extension_ in the request body.
 
The following is the syntax of the requests. For more information on creating such resource instances,
see the corresponding topics for creating a [message](../api/user_post_messages.md), [event](../api/user_post_events.md), 
[contact](../api/user_post_contacts.md), or [group event](../api/group_post_groups.md). 

```http
POST /me/messages
POST /users/<objectId>/messages

POST /me/events
POST /users/<objectId>/events

POST /me/contacts
POST /users/<objectId>/contacts

POST /groups/<gId>/events

```

To create an extension in an existing resource instance, specify the instance in the
request, and include the extension in the request body.

```http
POST /me/messages/<id>/extensions
POST /users/<objectId>/messages/<id>/extensions

POST /me/events/<id>/extensions
POST /users/<objectId>/events/<id>/extensions

POST /me/contacts/<id>/extensions
POST /users/<objectId>/contacts/<id>/extensions

POST /groups/<gId>/events/<id>/extensions
```


### Parameters
|**Parameter**|**Type**|**Description**|
|:-----|:-----|:-----|
|_URL parameters_|
|id|string|A unique identifier for an instance of a resource (message, event, or contact). Required.|
|objectId|string|A unique identifier for the signed-in user. Required.|
|gId|string|A unique group ID. Required.|


### Request headers
| Name       | Value |
|:---------------|:----------|
| Authorization | Bearer %token%|
| Content-Type | application/json |

### Request body

Provide a JSON body of an [openTypeExtension](../resources/openTypeExtension.md), with the following required
name-value pairs, and any additional custom data:

| Name       | Value |
|:---------------|:----------|
| @odata.type | Microsoft.Graph.OpenTypeExtension |
| ExtensionName | %unique_string% |

When creating an extension in a new resource instance, in addition to the **openTypeExtension** object, 
provide a JSON representation of that resource instance ([message](../resources/message.md), 
[event](../resources/event.md), or [contact](../resources/contact.md) object).

### Response

If successful, this method returns a `201 Created` response code.

When creating an extension in a new resource instance, the 
response body includes the new instance (a [message](../resources/message.md), 
[event](../resources/event.md), or [contact](../resources/contact.md) object) expanded with the
[openTypeExtension](../resources/openTypeExtension.md).

When creating an extension in an existing resource instance, the response body includes 
just the **openTypeExtension** object.
 


### Example
##### Request

The first example creates a message and an extension in the same call. The request body includes the following:
- The **Subject**, **Body**, and **ToRecipients** properties typical of a new message. 
- And for the extension:
  - The type `Microsoft.Graph.OpenTypeExtension`. 
  - The extension name "Com.Contoso.Referral". 
  - Additional data to be stored as 3 custom properties in the JSON payload: `CompanyName`, `ExpirationDate`, and `DealValue`.  

```http
POST https://graph.microsoft.com/beta/me/messages

{
  "Subject": "Annual review",
  "Body": {
    "ContentType": "HTML",
    "Content": "You should be proud!"
  },
  "ToRecipients": [
    {
      "EmailAddress": {
        "Address": "rufus@contoso.com"
      }
    }
  ],
  "Extensions": [
    {
      "@odata.type": "Microsoft.Graph.OpenTypeExtension",
      "ExtensionName": "Com.Contoso.Referral",
      "CompanyName": "Wingtip Toys",
      "ExpirationDate": "2015-12-30T11:00:00.000Z",
      "DealValue": 10000
    }
  ]
}
```

****

The second example creates an extension in the specified message. The request body includes the following for the 
extension:
- The type `Microsoft.Graph.OpenTypeExtension`. 
- The extension name "Com.Contoso.Referral".
- Additional data to be stored as 3 custom properties in the JSON payload: `CompanyName`, `DealValue`, and `ExpirationDate`.  
 
```http
POST https://graph.microsoft.com/beta/me/messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions

{ 
  "@odata.type" : "Microsoft.Graph.OpenTypeExtension", 
  "ExtensionName" : "Com.Contoso.Referral", 
  "CompanyName" : "Wingtip Toys", 
  "DealValue" : 500050, 
  "ExpirationDate" : "2015-12-03T10:00:00.000Z" 
} 
```

****

The third example creates an extension in the specified group event. The request body includes the following for the 
extension:
- The type `Microsoft.Graph.OpenTypeExtension`. 
- The extension name "Com.Contoso.Deal".
- Additional data to be stored as 3 custom properties in the JSON payload: `CompanyName`, `DealValue`, and `ExpirationDate`.  
  
```http
POST /groups('f5480dfd-7d77-4d0b-ba2e-3391953cc74a')/events('AAMkADVl17IsAAA=')/extensions 

{
  "@odata.type" : "Microsoft.Graph.OpenTypeExtension",
  "ExtensionName" : "Com.Contoso.Deal",
  "CompanyName" : "Alpine Skis",
  "DealValue" : 1010100,
  "ExpirationDate" : "2015-07-03T13:04:00.000Z"
}
```

****


##### Response

Here is the response for the first example request. The response body includes properties of the new message, 
and the following for the new extension:
- The **Id** property with the fully qualified name of `Microsoft.Graph.OpenTypeExtension.Com.Contoso.Referral`. 
- The default property **ExtensionName** specified in the request.
- The custom data specified in the request stored as 3 custom properties.

```http
HTTP/1.1 201 OK
Content-type: application/json

{
  "@odata.context": "https://graph.microsoft.com/beta/$metadata#Me/Messages/$entity",
  "@odata.id": "https://graph.microsoft.com/beta/Users('ddfc984d-b826-40d7-b48b-57002df800e5@1717f226-49d1-4d0c-9d74-709fad664b77')/Messages
('AAMkAGEbs88AAB84uLuAAA=')",
  "@odata.etag": "W/\"CQAAABYAAACY4MQpaFz9SbqUDe4+bs88AAB88LOj\"",
  "Id": "AAMkAGEbs88AAB84uLuAAA=",
  "CreatedDateTime": "2015-10-30T03:03:43Z",
  "LastModifiedDateTime": "2015-10-30T03:03:43Z",
  "ChangeKey": "CQAAABYAAACY4MQpaFz9SbqUDe4+bs88AAB88LOj",
  "Categories": [ ],
  "ReceivedDateTime": "2015-10-30T03:03:43Z",
  "SentDateTime": "2015-10-30T03:03:43Z",
  "HasAttachments": false,
  "Subject": "Annual review",
  "Body": {
    "ContentType": "HTML",
    "Content": "<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=utf-8\">\r
\n<meta content=\"text/html; charset=us-ascii\">\r\n</head>\r\n<body>\r\nYou should be proud!\r\n</body>\r
\n</html>\r\n"
  },
  "BodyPreview": "You should be proud!",
  "Importance": "Normal",
  "ParentFolderId": "AQMkAGEwAAAIBDwAAAA==",
  "Sender": null,
  "From": null,
  "ToRecipients": [
    {
      "EmailAddress": {
        "Address": "rufus@contoso.com",
        "Name": "John Doe"
      }
    }
  ],
  "CcRecipients": [ ],
  "BccRecipients": [ ],
  "ReplyTo": [ ],
  "ConversationId": "AAQkAGEFGugh3SVdMzzc=",
  "IsDeliveryReceiptRequested": false,
  "IsReadReceiptRequested": false,
  "IsRead": true,
  "IsDraft": true,
  "WebLink": "https://outlook.office.com/owa/?
ItemID=AAMkAGEbs88AAB84uLuAAA%3D&exvsurl=1&viewmodel=ReadMessageItem",
  "MentionedMe": null,
  "Mentioned": [ ],
  "InferenceClassification": "Focused",
  "Extensions@odata.context": "https://graph.microsoft.com/beta/$metadata#Me/Messages
('AAMkAGEbs88AAB84uLuAAA%3D')/Extensions",
  "Extensions": [
    {
      "@odata.type": "#Microsoft.Graph.OpenTypeExtension",
      "@odata.id": "https://graph.microsoft.com/beta/Users('ddfc984d-b826-40d7-b48b-57002df800e5@1717f226-49d1-4d0c-9d74-709fad664b77')/Messages
('AAMkAGEbs88AAB84uLuAAA=')/extensions('Microsoft.Graph.OpenTypeExtension.Com.Contoso.Referral')",
      "Id": "Microsoft.Graph.OpenTypeExtension.Com.Contoso.Referral",
      "ExtensionName": "Com.Contoso.Referral",
      "CompanyName": "Wingtip Toys",
      "ExpirationDate": "2015-12-30T11:00:00.000Z",
      "DealValue": 10000
    }
  ]
}
```

****

Here is the response for the second example request. The response body includes the following for the new extension:
- The default property **ExtensionName**.
- The **Id** property with the fully qualified name of `Microsoft.Graph.OpenTypeExtension.Com.Contoso.Referral`. 
- The custom data to be stored.  

```http
HTTP/1.1 201 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Me/Messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/Extensions/$entity",
    "@odata.type": "#Microsoft.Graph.OpenTypeExtension",
    "@odata.id": "https://graph.microsoft.com/beta/Users('ddfc984d-b826-40d7-b48b-57002df85e00@1717f226-49d1-4d0c-9d74-709fad6677b4')/Messages('AAMkAGE1M2IyNGNmLTI5MTktNDUyZi1iOTVl===')/extensions
('Microsoft.Graph.OpenTypeExtension.Com.Contoso.Referral')",
    "ExtensionName": "Com.Contoso.Referral",
    "Id": "Microsoft.Graph.OpenTypeExtension.Com.Contoso.Referral",
    "CompanyName": "Wingtip Toys",
    "DealValue": 500050,
    "ExpirationDate": "2015-12-03T10:00:00.000Z"
}
```

****

Here is the response from the third example request.

```
{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#groups('f5480dfd-7d77-4d0b-ba2e-3391953cc74a')/Events('AAMkADVl7IsAAA%3D')/Extensions/$entity",
    "@odata.type": "#Microsoft.Graph.OpenTypeExtension",
    "Id": "Microsoft.Graph.OpenTypeExtension.Com.Contoso.Deal",
    "ExtensionName": "Com.Contoso.Deal",
    "CompanyName": "Alpine Skis",
    "DealValue": 1010100,
    "ExpirationDate": "2015-07-03T13:04:00Z"
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