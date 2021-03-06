# Create page

Create a new OneNote page in the default section of the default notebook.

To create a page in a different section in the default notebook, you can use the `sectionName` query parameter.  Example: `../notes/pages?sectionName=My%20section`

The `POST /notes/pages` operation is used only to create pages in the current user's default notebook. If you're targeting other notebooks, you can [create pages in a specified section](../api/section_post_pages.md).           
### Prerequisites
One of the following **scopes** is required to execute this API:  
Notes.Create, Notes.ReadWrite.CreatedByApp, Notes.ReadWrite, or Notes.ReadWrite.All
### HTTP request
<!-- { "blockType": "ignored" } -->

```http
POST /me/notes/pages
POST /users/<mail>/notes/pages
POST /users/<objectId>/notes/pages
POST /groups/<objectId>/notes/pages
```

### Request headers  
| Name       | Type | Description|
|:---------------|:--------|:----------|
| Authorization  | string  | `Bearer <token>` A valid OAuth token provided to the app based on the user credentials and the user having authorized access. |
| Content-Type | string | `text/html` or `application/xhtml+xml` for the HTML content, including for the required "Presentation" part of multipart requests. Multipart requests use the `multipart/form-data; boundary=your-boundary` content type. |

### Request body
In the request body, supply the HTML content for the page.

The body can contain HTML placed directly in the request body, or it can contain a multipart message format as shown in the example. If you're sending binary data, then you must send a multipart request.

### Response
If successful, this method returns a `201 Created` response code and the new [page](../resources/page.md) object in the response body.

### Example
##### Request
Here is an example of the request.

In the `../notes/pages` path, you can use the `sectionName` query parameter to create a page in a specific section in the default notebook. Example: `../notes/pages?sectionName=My%20section`. If the section doesn't exist (or was renamed), the API will create a new section.

<!-- {
  "blockType": "request",
  "name": "create_page_from_notes"
}-->
```http
<<<<<<< HEAD
POST https://graph.microsoft.com/beta/me/notes/pages
Content-length: 312
Content-type: multipart/form-data; boundary=MyPartBoundary198374

--MyPartBoundary198374
Content-Disposition:form-data; name="Presentation"
Content-Type:text/html

<!DOCTYPE html>
<html>
  <head>
    <title>A page with <i>rendered</i> images and an <b>attached</b> file</title>
    <meta name="created" content="2015-07-22T09:00:00-08:00" />
  </head>
  <body>
    <p>Here's an image from an online source:</p>
    <img src="http://..." alt="an image on the page" width="500" />
    <p>Here's an image uploaded as binary data:</p>
    <img src="name:imageBlock1" alt="an image on the page" width="300" />
    <p>Here's a file attachment:</p>
    <object data-attachment="FileName.pdf" data="name:fileBlock1" type="application/pdf" />
  </body>
</html>

--MyPartBoundary198374
Content-Disposition:form-data; name="imageBlock1"
Content-Type:image/jpeg

... binary image data ...

--MyPartBoundary198374
Content-Disposition:form-data; name="fileBlock1"
Content-Type:application/pdf

... binary file data ...

--MyPartBoundary198374--
```
##### Response
Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.page"
} -->
```http
Content-type: application/json
Content-length: 312

{
  "title": "title-value",
  "createdByAppId": "createdByAppId-value",
  "links": {
    "oneNoteClientUrl": {
      "href": "href-value"
    },
    "oneNoteWebUrl": {
      "href": "href-value"
    }
  },
  "contentUrl": "contentUrl-value",
  "content": "content-value",
  "lastModifiedTime": "datetime-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Page",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->