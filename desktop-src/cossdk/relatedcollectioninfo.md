---
Description: Retrieves information about other collections related to the collection from which it is called.
ms.assetid: daea5b23-6a13-46f4-89c8-0d93b614311e
title: RelatedCollectionInfo collection
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: interface
ms.date: 05/31/2018
---

# RelatedCollectionInfo collection

Retrieves information about other collections related to the collection from which it is called. The **RelatedCollectionInfo** collection is accessible from any [**COMAdminCatalogCollection**](/windows/desktop/api/ComAdmin/) object by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) method. The **RelatedCollectionInfo** collection contains one object for each collection that is accessible from the original collection. Related collections follow the Component Services administration tool collection hierarchy.

This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](/windows/desktop/api/ComAdmin/) object.

## Members

The **RelatedCollectionInfo** collection inherits from the [**IUnknown**](https://msdn.microsoft.com/library/windows/desktop/ms680509) interface but does not have additional members.

## Related Collections

You can navigate from this collection to any of the following collections:

-   [**PropertyInfo**](propertyinfo.md)
-   **RelatedCollectionInfo**

You can navigate to this collection from every collection.

## Properties

The following properties are supported by the [**COMAdminCatalogObject**](/windows/desktop/api/ComAdmin/) object within the collection:

-   [Name](#name)

### Name



|                |                                                                                                                                                                                                            |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Description    | The name of the related collection. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection. |
| Access         | ReadOnly                                                                                                                                                                                                   |
| Type           | String                                                                                                                                                                                                     |
| Default        | None                                                                                                                                                                                                       |
| Minimum system | Windows 2000                                                                                                                                                                                               |



 

## See also

<dl> <dt>

[COM+ Administration Collections](com--administration-collections.md)
</dt> </dl>

 

 


