---
title: "DriveItemVersion resource type"
description: "The **DriveItemVersion** resource represents a specific version of a DriveItem."
ms.localizationpriority: medium
ms.prod: "sharepoint"
author: "JeremyKelley"
doc_type: resourcePageType
---

# DriveItemVersion resource type

Namespace: microsoft.graph

The **DriveItemVersion** resource represents a specific version of a [DriveItem](driveitem.md).


## Tasks on DriveItemVersion resources

The following tasks are available for driveItemVersion resources.

|            Common task             |         HTTP method         |
| :--------------------------------- | :-------------------------- |
| [List versions][version-list]      | `GET /drive/items/{item-id}/versions`  |
| [Get version][version-get]         | `GET /drive/items/{item-id}/versions/{version-id}`     |
| [Get contents][content-get]        | `GET /drive/items/{item-id}/versions/{version-id}/content` |
| [Restore version][version-restore] | `POST /drive/items/{item-id}/versions/{version-id}/restoreversion` |

[version-list]: ../api/driveitem-list-versions.md
[version-get]: ../api/driveitemversion-get.md
[content-get]: ../api/driveitemversion-get-contents.md
[version-restore]: ../api/driveitemversion-restore.md

In the previous table, the examples use `/drive`, but there are many valid requests.

## JSON representation

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.baseItemVersion",
  "@odata.type": "microsoft.graph.driveItemVersion",
  "@type.aka": "oneDrive.driveItemVersion"
}-->

```json
{
  "content": { "@odata.type": "Edm.Stream" },
  "id": "string",
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "2016-01-01T15:20:01.125Z",
  "publication": { "@odata.type": "microsoft.graph.publicationFacet" },
  "size": 12356
}
```

## Properties

|      Property name       |                         Type                         |                               Description                               |
| :----------------------- | :--------------------------------------------------- | :---------------------------------------------------------------------- |
| **id**                   | string                                               | The ID of the version. Read-only.                                       |
| **lastModifiedBy**       | [IdentitySet](../resources/identityset.md)           | Identity of the user which last modified the version. Read-only.        |
| **lastModifiedDateTime** | [DateTimeOffset](../resources/timestamp.md)          | Date and time the version was last modified. Read-only.                 |
| **publication**          | [PublicationFacet](../resources/publicationfacet.md) | Indicates the publication status of this particular version. Read-only. |
| **size**                 | Int64                                                | Indicates the size of the content stream for this version of the item.  |
| **content**              | Stream                                               | The content stream for this version of the item.                        |

<!-- {
  "type": "#page.annotation",
  "description": "The version facet provides information about the properties of a file version.",
  "keywords": "version,versions,version-history,history",
  "section": "documentation",
  "tocPath": "Facets/Version"
} -->

