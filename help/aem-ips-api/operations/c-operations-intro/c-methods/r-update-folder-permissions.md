---
description: Atualizar permissões de pasta.
solution: Experience Manager
title: updateFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 4e4f382e-4339-4b9d-a721-d33a4fa8be6b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---

# updateFolderPermissions{#updatefolderpermissions}

Atualizar permissões de pasta.

Sintaxe

## Tipos de usuário autorizados {#section-e5c2217231bf4b3386e0ab3f2e9aca0b}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-339e6e17c5504e1ea79fbdc05f618050}

**Entrada (updateFolderPermissionsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | Identificador da empresa. |
| folderHandle | `xsd:string` | Sim | Identificador de pasta. |
| updateChildren | `xsd:boolean` | Sim | Determina se os filhos devem ser atualizados com permissões definidas para a pasta de nível superior. |
| updateArray | `types:PermissionUpdateArray` | Sim | A matriz de atualizações de permissão que você deseja aplicar à pasta. |

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
