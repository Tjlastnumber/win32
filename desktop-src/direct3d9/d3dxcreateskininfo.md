---
Description: Creates an empty skin mesh object using a declarator.
ms.assetid: c98da2e5-a9eb-4070-8846-b346b5c57fb3
title: D3DXCreateSkinInfo function
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# D3DXCreateSkinInfo function

Creates an empty skin mesh object using a declarator.

## Syntax


```C++
HRESULT D3DXCreateSkinInfo(
  _In_        DWORD             NumVertices,
  _In_  const D3DVERTEXELEMENT9 *pDeclaration,
  _In_        DWORD             NumBones,
  _Out_       LPD3DXSKININFO    *ppSkinInfo
);
```



## Parameters

<dl> <dt>

*NumVertices* \[in\]
</dt> <dd>

Type: **[**DWORD**](https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46)**

Number of vertices for the skin mesh.

</dd> <dt>

*pDeclaration* \[in\]
</dt> <dd>

Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***

Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.

</dd> <dt>

*NumBones* \[in\]
</dt> <dd>

Type: **[**DWORD**](https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46)**

Number of bones for the skin mesh.

</dd> <dt>

*ppSkinInfo* \[out\]
</dt> <dd>

Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)\***

Address of a pointer to an [**ID3DXSkinInfo**](id3dxskininfo.md) interface, representing the created skin mesh object.

</dd> </dl>

## Return value

Type: **[**HRESULT**](https://msdn.microsoft.com/windows/desktop/455d07e9-52c3-4efb-a9dc-2955cbfd38cc)**

If the function succeeds, the return value is D3D\_OK. If the function fails, the return value can be: E\_OUTOFMEMORY.

## Remarks

Use [**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md) to populate the empty skin mesh object returned by this method.

## Requirements



|                    |                                                                                        |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## See also

<dl> <dt>

[Mesh Functions](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**SetBoneInfluence**](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 



