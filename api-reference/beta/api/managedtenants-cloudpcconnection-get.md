---
title: "Get cloudPcConnection"
description: "Read the properties and relationships of a cloudPcConnection object."
author: "isaiahwilliams"
localization_priority: Normal
ms.prod: "microsoft-365-lighthouse"
doc_type: apiPageType
---

# Get cloudPcConnection
Namespace: microsoft.graph.managedTenants

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Read the properties and relationships of a [cloudPcConnection](../resources/managedtenants-cloudpcconnection.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|CloudPC.Read.All, CloudPC.ReadWrite.All|
|Delegated (personal Microsoft account)|Not supported.|
|Application|Not supported.|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /tenantRelationships/managedTenants/cloudPcConnections/{cloudPcConnectionId}
```

## Optional query parameters
This method supports the [OData query parameters](/graph/query-parameters) to help customize the response, including `$apply`, `$count`, `$filter`, `$orderBy`, `$select`, `$skip`, and `$top`.

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a [cloudPcConnection](../resources/managedtenants-cloudpcconnection.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "sampleKeys": ["86789ee0-e31d-4bee-98e6-6f310bd327bb"],
  "name": "get_cloudpcconnection"
}
-->
``` http
GET https://graph.microsoft.com/beta/tenantRelationships/managedTenants/cloudPcConnections/86789ee0-e31d-4bee-98e6-6f310bd327bb
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.managedTenants.cloudPcConnection"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.managedTenants.cloudPcConnection",
  "id": "86789ee0-e31d-4bee-98e6-6f310bd327bb",
  "lastUpdated": "2021-07-11T15:46:28.1243279Z",
  "displayName": "Az-Connection-93ac6d62-7d78-4477-bd43-db5e2013864d",
  "healthCheckStatus": "Failed",
  "tenantId": "aa060093-1e81-45b4-bebc-652713194ef7",
  "tenantDisplayName": "Lucerne Publishing",
  "lastRefreshedDateTime": "2021-07-11T15:46:28.1243279Z"
}
```