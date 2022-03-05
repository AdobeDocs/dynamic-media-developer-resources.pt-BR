---
description: Usado por MetadataField/type, saveMetadataFieldParam/fieldType e createMetadataField/fieldType.
solution: Experience Manager
title: Tipos de campo de metadados
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---

# Tipos de campo de metadados{#metadata-field-types}

Usado por MetadataField/type, saveMetadataFieldParam/fieldType e createMetadataField/fieldType.

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
* [!DNL `MultiFixedTag`]: Zero ou mais valores de string de um dicionário fechado. Somente usuários administradores podem modificar o dicionário.
* [!DNL `MultiTag`]: Zero ou mais valores de string.
* [!DNL `SingleFixedTag`]: Um único valor de string de um dicionário fechado. If `setAssetMetadata` ou `batchSetAssetMetadata` são chamados com um valor que não está no dicionário, uma falha é retornada. Somente usuários administradores podem modificar o dicionário.

* [!DNL `SingleTag`]: Qualquer valor de string único.
* [!DNL `String`]
