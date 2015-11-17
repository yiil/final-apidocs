# Create subscription

Use this API to create a new subscription.
### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->

```http
POST /subscriptions

```
### Optional query parameters
This method supports the [OData Query Parameters](http://graph.microsoft.io/docs/overview/query_parameters) to help customize the response.

### Request headers
| Name       | Type | Description|
|:-----------|:------|:----------|
| Authorization  | string  | Bearer <token>. Required. |


### Response
If successful, this method returns `201, Created` response code and [subscription](../resources/subscription.md) object in the response body.

### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "create_subscription_from_subscriptions"
}-->
```http
POST https://graph.microsoft.com/beta/subscriptions
Content-type: application/json
Content-length: 208

{
  "resource": "resource-value",
  "changeType": "changeType-value",
  "clientState": "clientState-value",
  "notificationUrl": "notificationUrl-value",
  "subscriptionExpirationDateTime": "datetime-value"
}
```
In the request body, supply a JSON representation of [subscription](../resources/subscription.md) object.
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.subscription"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 252

{
  "subscriptionId": "subscriptionId-value",
  "resource": "resource-value",
  "changeType": "changeType-value",
  "clientState": "clientState-value",
  "notificationUrl": "notificationUrl-value",
  "subscriptionExpirationDateTime": "datetime-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create subscription",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->