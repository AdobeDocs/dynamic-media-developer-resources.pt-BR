---
description: Usado por MetadataField/type, saveMetadataFieldParam/fieldType e createMetadataField/fieldType.
seo-description: Usado por MetadataField/type, saveMetadataFieldParam/fieldType e createMetadataField/fieldType.
seo-title: Tipos de campo de metadados
solution: Experience Manager
title: Tipos de campo de metadados
topic: Dynamic Media Image Production System API
uuid: 57d292bb-848a-4e6e-bd08-4e6af1f9fc72
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '107'
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
* [!DNL `MultiTag`]: Valores de string zero ou mais.
* [!DNL `SingleFixedTag`]: Um único valor de string de um dicionário fechado. Se `setAssetMetadata` ou `batchSetAssetMetadata` forem chamados com um valor que não esteja no dicionário, uma falha será retornada. Somente usuários administradores podem modificar o dicionário.

* [!DNL `SingleTag`]: Qualquer valor de string único.
* [!DNL `String`]

