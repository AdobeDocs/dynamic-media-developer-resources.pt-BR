---
description: Usado por MetadataField/type, saveMetadataFieldParam/fieldType e createMetadataField/fieldType.
solution: Experience Manager
title: Tipos de campo de metadados
feature: Dynamic Media Classic, SDK/API, Metadados
role: Developer,Administrator
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# Tipos de campo de metadados{#metadata-field-types}

Usado por MetadataField/type, saveMetadataFieldParam/fieldType e createMetadataField/fieldType.

Sintaxe

## Valores {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]: Um caso especial de  [!DNL `SingleFixedTag`] com um dicionário não modificável inicializado para os valores  [!DNL `True`] e  [!DNL `False`].

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]: Zero ou mais valores de string de um dicionário fechado. Somente usuários administradores podem modificar o dicionário.
* [!DNL `MultiTag`]: Zero ou mais valores de string.
* [!DNL `SingleFixedTag`]: Um único valor de string de um dicionário fechado. Se `setAssetMetadata` ou `batchSetAssetMetadata` forem chamados com um valor que não esteja no dicionário, uma falha será retornada. Somente usuários administradores podem modificar o dicionário.

* [!DNL `SingleTag`]: Qualquer valor de string único.
* [!DNL `String`]
