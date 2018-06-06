---
Description: Creates a temporary container in the cryptographic service provider (CSP) and loads a private key from memory into the container.
ms.assetid: 9388b49b-fad4-4499-a391-fe58ed672552
title: PvkPrivateKeyAcquireContextFromMemory function
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# PvkPrivateKeyAcquireContextFromMemory function

> \[!Important\]  
> This API is deprecated. Microsoft may remove this API in future releases.

 

The **PvkPrivateKeyAcquireContextFromMemory** function creates a temporary container in the [*cryptographic service provider*](https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb) (CSP) and loads a [*private key*](https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a) from memory into the container.

> [!Note]  
> This function has no associated header file or import library. To call this function, you must create a user-defined header file and use the [**LoadLibrary**](https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65) and [**GetProcAddress**](https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597) functions to dynamically link to Mssign32.dll.

 

## Syntax


```C++
BOOL WINAPI PvkPrivateKeyAcquireContextFromMemory(
  _In_        LPCWSTR    pwszProvName,
  _In_        DWORD      dwProvType,
  _In_        BYTE       *pbData,
  _In_        DWORD      cbData,
  _In_        HWND       hwndOwner,
  _In_        LPCWSTR    pwszKeyName,
  _Inout_opt_ DWORD      *pdwKeySpec,
  _Out_       HCRYPTPROV *phCryptProv,
  _Out_       LPTSTR     *ppwszTmpContainer
);
```



## Parameters

<dl> <dt>

*pwszProvName* \[in\]
</dt> <dd>

A pointer to a null-terminated string that contains the name of the CSP whose type is requested in *dwProvType*.

</dd> <dt>

*dwProvType* \[in\]
</dt> <dd>

A **DWORD** value for the CSP type. For more information about CSP types, see [Cryptographic Provider Types](cryptographic-provider-types.md).

</dd> <dt>

*pbData* \[in\]
</dt> <dd>

A pointer to a buffer to receive the context data. The caller must provide this resource.

</dd> <dt>

*cbData* \[in\]
</dt> <dd>

A **DWORD** value that specifies the size, in bytes, of the *pbData* buffer. The caller must provide this value.

</dd> <dt>

*hwndOwner* \[in\]
</dt> <dd>

If a password is required to decrypt the context data pointed to by the *pbData* parameter, this parameter is a handle to the parent of the dialog box; otherwise, it is **NULL**.

</dd> <dt>

*pwszKeyName* \[in\]
</dt> <dd>

A pointer to a null-terminated string that contains the name of the key to retrieve.

</dd> <dt>

*pdwKeySpec* \[in, out, optional\]
</dt> <dd>

A pointer to a **DWORD** value that specifies the type of key. Possible values include **AT\_KEYEXCHANGE** or **AT\_SIGNATURE**.

</dd> <dt>

*phCryptProv* \[out\]
</dt> <dd>

A pointer to a handle for the CSP.

</dd> <dt>

*ppwszTmpContainer* \[out\]
</dt> <dd>

The address of a pointer to a null-terminated string for the temporary container name. The **PvkPrivateKeyAcquireContextFromMemory** function provides the buffer for this string and initializes it. When calling **PvkPrivateKeyAcquireContextFromMemory**, the address should point to a **NULL** value.

</dd> </dl>

## Return value

Upon success, this function returns **TRUE**. The **PvkPrivateKeyAcquireContextFromMemory** function returns **FALSE** if it fails.

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows XP \[desktop apps only\]<br/>                                             |
| Minimum supported server<br/> | Windows Server 2003 \[desktop apps only\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



 

 



