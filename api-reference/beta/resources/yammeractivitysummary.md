---
title: "yammerActivitySummary resource type"
description: "The following is a JSON representation of the resource."
ms.localizationpriority: medium
ms.prod: "reports"
author: "sarahwxy"
doc_type: resourcePageType
---

# yammerActivitySummary resource type

Namespace: microsoft.graph

## Properties

| Property          | Type   |
| :---------------- | :----- |
| reportRefreshDate | Date   |
| liked             | Int64  |
| posted            | Int64  |
| read              | Int64  |
| reportDate        | Date   |
| reportPeriod      | String |

## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.yammerActivitySummary"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "liked": 1024, 
  "posted": 1024, 
  "read": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```


