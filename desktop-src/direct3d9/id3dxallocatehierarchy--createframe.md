---
Description: Requests allocation of a frame object.
ms.assetid: 977e40d6-bf49-44b6-ac95-88e7f778ea50
title: ID3DXAllocateHierarchy::CreateFrame method
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# ID3DXAllocateHierarchy::CreateFrame method

Requests allocation of a frame object.

## Syntax


```C++
HRESULT CreateFrame(
  [in]          LPCSTR      Name,
  [out, retval] LPD3DXFRAME *ppNewFrame
);
```



## Parameters

<dl> <dt>

*Name* \[in\]
</dt> <dd>

Type: **[**LPCSTR**](https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46)**

Name of the frame to be created.

</dd> <dt>

*ppNewFrame* \[out, retval\]
</dt> <dd>

Type: **[**LPD3DXFRAME**](d3dxframe.md)\***

Returns the created frame object.

</dd> </dl>

## Return value

Type: **[**HRESULT**](https://msdn.microsoft.com/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

The return values of this method are implemented by an application programmer. In general, if no error occurs, program the method to return D3D\_OK. Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.

## Requirements



|                    |                                                                                        |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## See also

<dl> <dt>

[ID3DXAllocateHierarchy](id3dxallocatehierarchy.md)
</dt> </dl>

 

 



