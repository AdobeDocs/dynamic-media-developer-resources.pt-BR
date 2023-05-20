---
description: Usado por MetadataField/tipo, saveMetadataFieldParam/fieldType e createMetadataField/fieldType.
solution: Experience Manager
title: Tipos de campos de metadados
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---

# Tipos de campos de metadados{#metadata-field-types}

Usado por MetadataField/tipo, saveMetadataFieldParam/fieldType e createMetadataField/fieldType.

Sintaxe

## Valores {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]: um caso especial de [!DNL `SingleFixedTag`] com um dicionário não modificável inicializado para os valores [!DNL `True`] e [!DNL `False`].

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]: zero ou mais valores de sequência de caracteres de um dicionário fechado. Somente usuários administradores podem modificar o dicionário.
* [!DNL `MultiTag`]: zero ou mais valores da string.
* [!DNL `SingleFixedTag`]: um único valor de string de um dicionário fechado. Se `setAssetMetadata` ou `batchSetAssetMetadata` são chamados com um valor fora do dicionário, uma falha é retornada. Somente usuários administradores podem modificar o dicionário.

* [!DNL `SingleTag`]: qualquer valor único de string.
* [!DNL `String`]
