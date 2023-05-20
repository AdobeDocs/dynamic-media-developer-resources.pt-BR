---
description: As configurações nesta seção se aplicam às respostas do conjunto de mídia obtidas pelo modificador req=set.
solution: Experience Manager
title: Respostas do conjunto de mídias
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e3833726-d345-4741-8096-d74f299ac9fc
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Respostas do conjunto de mídias{#media-set-responses}

As configurações nesta seção se aplicam às respostas do conjunto de mídia obtidas pelo modificador req=set.

## PS::fvctx.useCatalogRecordValidation - Política de armazenamento em cache {#section-9accb087d16548a988993bb30395a6f6}

Essa propriedade controla a política de cache ao determinar se a resposta definida recuperada do cache precisa ou não ser gerada novamente. Se a propriedade estiver desativada, o carimbo de data e hora do [!DNL catalog.ini] arquivo é usado para validação. Se a propriedade estiver ativada, a última `catalog::LastModified` o carimbo de data e hora de todos os registros referenciados é usado para validação.

## PS::fvctx.nestedLimit - Limite de aninhamento {#section-280210341f1647fea02590e7069934d2}

A profundidade máxima de aninhamento de qualquer `req=set` resposta. Se essa profundidade for excedida, um erro será retornado.

## PS::fvctx.brochureLimit - Limite do folheto {#section-fe36e47db49244cea7f07e9dd3639440}

O número máximo de brochuras de catálogo eletrônico no `req=set` que contém todos os metadados associados. Quando esse limite for excedido, todos os mapas privados e dados do usuário associados ao item de folheto serão suprimidos.
