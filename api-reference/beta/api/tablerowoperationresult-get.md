---
title: "Get tableRowOperationResult"
description: "Async operation result for addTableRow operation"
author: "lumine2008"
localization_priority: Normal
ms.prod: "excel"
doc_type: apiPageType
---

# Get tableRowOperationResult
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

This api will get async operation result for create TableRow [Get workbookoperation](./workbookoperation-get.md), after you get 'succeeded' operationStatus and it indicate you to get the result from this request.

For full scenario of this async operation, please refer to [Create TableRow](./table-post-rows.md).

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|Files.ReadWrite|
|Delegated (personal Microsoft account)|Not supported.|
|Application|Not supported.|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /driveItem/workbook/tableRowOperationResult
```

## Function parameters
In the request URL, provide the following query parameters with values.
The following table shows the parameters that can be used with this function.

|Parameter|Type|Description|
|:---|:---|:---|
|key|String|The operationid provided in the workbookoperation response|


## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Optional.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this function returns a `200 OK` response code and a [workbookTableRow](../resources/workbooktablerow.md) in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "workbook_tablerowoperationresult"
}
-->
``` http
GET https://graph.microsoft.com/beta/driveItem/workbook/tableRowOperationResult(key='parameterValue')
```


### Response

Here is an example of the response

>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookTableRow"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "index": 99,
  "values": "[[1, 2, 3]]"
}
```