---
description: As configurações nesta seção se aplicam às respostas do conjunto de mídia obtidas pelo modificador req=set.
solution: Experience Manager
title: Respostas do conjunto de mídia
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# Respostas do conjunto de mídia{#media-set-responses}

As configurações nesta seção se aplicam às respostas do conjunto de mídia obtidas pelo modificador req=set.

## PS::fvctx.useCatalogRecordValidation - Política de Cache {#section-9accb087d16548a988993bb30395a6f6}

Essa propriedade controla a política de cache ao determinar se a resposta de conjunto recuperada do cache precisa ou não ser regerada. Se a propriedade estiver desativada, o carimbo de data e hora do arquivo [!DNL catalog.ini] será usado para validação. Se a propriedade estiver ativada, o carimbo de data e hora `catalog::LastModified` mais recente de todos os registros referenciados será usado para validação.

## PS::fvctx.nestingLimit - Limite de aninhamento {#section-280210341f1647fea02590e7069934d2}

A profundidade máxima de aninhamento de qualquer resposta `req=set`. Se essa profundidade for excedida, um erro será retornado.

## PS::fvctx.brochureLimit - Limite do folheto {#section-fe36e47db49244cea7f07e9dd3639440}

O número máximo de brochuras de catálogo eletrônico na resposta `req=set` que contém todos os metadados associados. Depois que esse limite for excedido, todos os mapas privados e dados do usuário associados ao item da brochura serão suprimidos.
