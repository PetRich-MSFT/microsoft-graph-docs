# message: createReplyAll

Create a draft of the Reply All message. You can then [update](../api/message_update.md) or 
[send](../api/message_send.md) the draft.

## Prerequisites
One of the following **scopes** is required to execute this API:
*Mail.ReadWrite*
## HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /me/messages/{id}/createReplyAll
POST /users/{id | userPrincipalName}/messages/{id}/createReplyAll
POST /me/mailFolders/{id}/messages/{id}/createReplyAll
POST /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/createReplyAll
```
## Request headers
| Name       | Type | Description|
|:---------------|:--------|:----------|
| Authorization  | string  | Bearer {token}. Required. |
| Content-Type | string  | Nature of the data in the body of an entity. Required. |

## Request body

## Response

If successful, this method returns `201, Created` response code and [Message](../resources/message.md) object in the response body.

## Example
Here is an example of how to call this API.
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "message_createreplyall"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/createReplyAll
Content-type: application/json
Content-length: 248

{
  "comment": "comment-value"
}
```

##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 248

{
  "receivedDateTime": "datetime-value",
  "sentDateTime": "datetime-value",
  "hasAttachments": true,
  "subject": "subject-value",
  "body": {
    "contentType": "",
    "content": "content-value"
  },
  "bodyPreview": "bodyPreview-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: createReplyAll",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
