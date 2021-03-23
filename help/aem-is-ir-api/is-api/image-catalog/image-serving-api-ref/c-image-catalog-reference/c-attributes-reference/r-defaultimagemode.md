---
description: Modo de imagem padrão. Seleciona como a imagem padrão é aplicada quando imagens especificadas na solicitação não são encontradas.
seo-description: Modo de imagem padrão. Seleciona como a imagem padrão é aplicada quando imagens especificadas na solicitação não são encontradas.
seo-title: DefaultImageMode
solution: Experience Manager
title: DefaultImageMode
uuid: e5640f09-e1e3-473b-8fbc-84c6bfce2460
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '132'
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
