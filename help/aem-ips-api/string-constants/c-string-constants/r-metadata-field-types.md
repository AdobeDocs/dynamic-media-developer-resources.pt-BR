---
description: Usado por MetadataField/tipo, saveMetadataFieldParam/fieldType e createMetadataField/fieldType.
solution: Experience Manager
title: Tipos de campos de metadados
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
TQID: 'https://experienceleague.adobe.com/XFRmGmRc9iE5xmW0P2KfDzc-X-3TTrNYWkzNieSodQc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 95
ht-degree: 0%

---

# Tipos de campos de metadados{#metadata-field-types}

Usado por MetadataField/tipo, saveMetadataFieldParam/fieldType e createMetadataField/fieldType.

Sintaxe

## Valores {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]: Um caso especial de [!DNL `SingleFixedTag`] com um dicionário não modificável inicializado para os valores [!DNL `True`] e [!DNL `False`].

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]: Zero ou mais valores de cadeia de caracteres de um dicionário fechado. Somente usuários administradores podem modificar o dicionário.
* [!DNL `MultiTag`]: zero ou mais valores de cadeia de caracteres.
* [!DNL `SingleFixedTag`]: um único valor de cadeia de caracteres de um dicionário fechado. Se `setAssetMetadata` ou `batchSetAssetMetadata` forem chamados com um valor que não está no dicionário, uma falha será retornada. Somente usuários administradores podem modificar o dicionário.

* [!DNL `SingleTag`]: Qualquer valor de cadeia de caracteres.
* [!DNL `String`]

