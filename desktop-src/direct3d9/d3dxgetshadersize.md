---
Description: Returns the size of the shader byte code, in bytes.
ms.assetid: 7dd091f7-fda9-49e1-982d-2eb57d9ecb23
title: D3DXGetShaderSize function
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# D3DXGetShaderSize function

Returns the size of the shader byte code, in bytes.

## Syntax


```C++
UINT D3DXGetShaderSize(
  _In_ const DWORD *pFunction
);
```



## Parameters

<dl> <dt>

*pFunction* \[in\]
</dt> <dd>

Type: **const [**DWORD**](https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46)\***

Pointer to the function DWORD stream.

</dd> </dl>

## Return value

Type: **[**UINT**](https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46)**

Returns the size of the shader byte code, in bytes.

## Requirements



|                    |                                                                                          |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Library<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## See also

<dl> <dt>

[Shader Functions](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 



