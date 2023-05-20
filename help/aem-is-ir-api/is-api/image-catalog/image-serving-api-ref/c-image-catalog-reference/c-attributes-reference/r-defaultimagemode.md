---
description: Modo de imagem padrão. Seleciona como a imagem padrão é aplicada quando imagens especificadas na solicitação não são encontradas.
solution: Experience Manager
title: DefaultImageMode
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b30ce72f-7c74-407c-bd4a-042b84c469e9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# DefaultImageMode{#defaultimagemode}

Modo de imagem padrão. Seleciona como a imagem padrão é aplicada quando imagens especificadas na solicitação não são encontradas.

## Propriedades {#section-7fa8acb63540490d9f5186231b5e77c3}

Enum. &#39;0&#39; para substituir toda a imagem composta, mesmo que a imagem ausente seja apenas uma das várias camadas; &#39;1&#39; para substituir cada imagem de origem de camada ausente pela imagem padrão e retornar o composto como de costume.

## Restrições {#section-04cb0d50e8914564a8d226d0d4663c8b}

O Servidor de imagens é revertido para `DefaultImageMode=0` ao renderizar imagem aninhada, FXG ou `req=set` falha nas solicitações.

## Padrão {#section-9e318524a2a5496386901286748c7ee7}

Herdado de `default::DefaultImage` se não estiver definido ou se estiver vazio.

## Consulte também {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) , [attribute::DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
