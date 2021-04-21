---
description: Modo de imagem padrão. Seleciona como a imagem padrão é aplicada quando imagens especificadas na solicitação não são encontradas.
solution: Experience Manager
title: DefaultImageMode
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---


# DefaultImageMode{#defaultimagemode}

Modo de imagem padrão. Seleciona como a imagem padrão é aplicada quando imagens especificadas na solicitação não são encontradas.

## Propriedades {#section-7fa8acb63540490d9f5186231b5e77c3}

Enum. &#39;0&#39; para substituir toda a imagem composta, mesmo que a imagem ausente seja apenas uma de várias camadas; &#39;1&#39; para substituir cada imagem de origem de camada ausente pela imagem padrão e retornar o composto como de costume.

## Restrições {#section-04cb0d50e8914564a8d226d0d4663c8b}

O Serviço de imagem reverte para `DefaultImageMode=0` quando as solicitações aninhadas de Renderização de imagem, FXG ou `req=set` falham.

## Padrão {#section-9e318524a2a5496386901286748c7ee7}

Herdado de `default::DefaultImage` se não estiver definido ou se estiver vazio.

## Consulte também {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) ,  [atributo::DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
