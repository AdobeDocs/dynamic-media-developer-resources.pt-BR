---
description: Atualize as permissões da pasta.
seo-description: Atualize as permissões da pasta.
seo-title: updateFolderPermissions
solution: Experience Manager
title: updateFolderPermissions
uuid: 940d7b63-80cf-4097-9cf9-8499b69181b7
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# updateFolderPermissions{#updatefolderpermissions}

Atualize as permissões da pasta.

Sintaxe

## Tipos de usuário autorizados {#section-e5c2217231bf4b3386e0ab3f2e9aca0b}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-339e6e17c5504e1ea79fbdc05f618050}

**Entrada (updateFolderPermissionsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | Manuseio da empresa. |
| `*`folderHandle`*` | `xsd:string` | Sim | Identificador de pasta. |
| `*`updateChildren`*` | `xsd:boolean` | Sim | Determina se deseja atualizar filhos com permissões definidas para a pasta de nível superior. |
| `*`updateArray`*` | `types:PermissionUpdateArray` | Sim | A matriz de atualizações de permissão que você deseja aplicar à pasta. |

**Saída (updateFolderPermissionsReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-c3fe4d4388674870a3856c35ef66b631}

**Solicitação**

```java
<ns1:updateFolderPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:updateChildren>false</ns1:updateChildren>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>true</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateFolderPermissionsParam>
```

**Resposta**

Nenhum.
