# Create task

Use this API to create a new task.
### Prerequisites
The following **scopes** are required to execute this API: 

Group.ReadWrite.All AND Tasks.ReadWrite

### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /tasks

```
### Request headers
| Name       | Type | Description|
|:---------------|:--------|:----------|
| Authorization  | string  | Value should be set to "Bearer (access-token)"|

### Request body
In the request body, supply a JSON representation of [task](../resources/task.md) object.


### Response
If successful, this method returns `201, Created` response code and [task](../resources/task.md) object in the response body.

### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "create_task_from_tasks"
}-->
```http
POST https://graph.microsoft.com/beta/tasks
Content-type: application/json
Content-length: 192

{
  "createdBy": "createdBy-value",
  "assignedTo": "assignedTo-value",
  "planId": "planId-value",
  "bucketId": "bucketId-value",
  "title": "title-value",
  "orderHint": "orderHint-value"
}
```
In the request body, supply a JSON representation of [task](../resources/task.md) object.
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.task"
} -->
```http
Content-type: application/json
Content-length: 192

{
  "createdBy": "createdBy-value",
  "assignedTo": "assignedTo-value",
  "planId": "planId-value",
  "bucketId": "bucketId-value",
  "title": "title-value",
  "orderHint": "orderHint-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create task",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->