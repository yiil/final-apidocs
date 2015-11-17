# subscription resource type



### JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.subscription"
}-->

```json
{
  "changeType": "string",
  "clientState": "string",
  "notificationUrl": "string",
  "resource": "string",
  "subscriptionExpirationDateTime": {"@odata.type": "microsoft.graph.dateTimeOffset"},
  "subscriptionId": "string (identifier)"
}

```
### Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|changeType|string||
|clientState|string||
|notificationUrl|string||
|resource|string||
|subscriptionExpirationDateTime|[dateTimeOffset](datetimeoffset.md)||
|subscriptionId|string| Read-only.|

### Relationships
None


### Methods

| Method		   | Return Type	|Description|
|:---------------|:--------|:----------|
|[Get subscription](../api/subscription_get.md) | [subscription](subscription.md) |Read properties and relationships of subscription object.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "subscription resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->