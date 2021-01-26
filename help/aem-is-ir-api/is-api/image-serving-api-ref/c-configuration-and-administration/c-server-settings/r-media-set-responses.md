---
description: As configurações nesta seção aplicam-se às respostas do conjunto de mídia obtidas pelo modificador req=set.
seo-description: As configurações nesta seção aplicam-se às respostas do conjunto de mídia obtidas pelo modificador req=set.
seo-title: Respostas de conjunto de mídia
solution: Experience Manager
title: Respostas de conjunto de mídia
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9fa6a38a-cd1f-499b-a2b6-e1a9a6c69ed0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---


# Respostas do conjunto de mídia{#media-set-responses}

As configurações nesta seção aplicam-se às respostas do conjunto de mídia obtidas pelo modificador req=set.

## PS::fvctx.useCatalogRecordValidation - política de cache {#section-9accb087d16548a988993bb30395a6f6}

Essa propriedade controla a política de cache ao determinar se a resposta definida recuperada do cache precisa ou não ser gerada novamente. Se a propriedade estiver desativada, o carimbo de data e hora do arquivo [!DNL catalog.ini] será usado para validação. Se a propriedade estiver ativada, o carimbo de data e hora mais recente `catalog::LastModified` de todos os registros referenciados será usado para validação.

## PS::fvctx.nestingLimit - Limite de aninhamento {#section-280210341f1647fea02590e7069934d2}

A profundidade máxima de aninhamento de qualquer resposta `req=set`. Se essa profundidade for excedida, um erro será retornado.

## PS::fvctx.brochureLimit - Limite de folheto {#section-fe36e47db49244cea7f07e9dd3639440}

O número máximo de folhetos de catálogo eletrônico na resposta `req=set` que contém todos os metadados associados. Quando esse limite for excedido, todos os mapas privados e dados do usuário associados ao item do folheto serão suprimidos.
