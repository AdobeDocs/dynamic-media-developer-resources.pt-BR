---
title: Solicitações do servidor de imagem incorporado
description: Uma solicitação do Servidor de imagem (IS) pode ser usada como uma imagem material.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# Solicitações do servidor de imagem incorporado{#embedded-image-server-requests}

Uma solicitação do Servidor de imagem (IS) pode ser usada como uma imagem material.

Especifique a solicitação no `src=` comando como segue:

` …&src=is( *[!DNL imageServingRequest]*)&…`

O `is` O token diferencia maiúsculas de minúsculas.

A solicitação aninhada não deve incluir o caminho raiz do Serviço de imagem (normalmente [!DNL http:// *[!DNL server]*/is/image/"]), mas pode incluir tokens de regras de pré-processamento.

Os seguintes comandos IS são ignorados quando especificados em solicitações aninhadas (no URL da solicitação ou em `catalog::Modifier` ou `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

Também são ignoradas `attribute::MaxPix` e `attribute::DefaultPix` do catálogo de imagens que se aplica à solicitação IS incorporada.

Se a imagem resultante da solicitação aninhada incluir dados de máscara (alfa), ela sempre será passada para o material. Use uma camada de imagem de fundo de cor sólida para evitar alfa indesejado.

O resultado da imagem de uma solicitação IS incorporada pode ser armazenado em cache opcionalmente incluindo `cache=on`. Por padrão, o armazenamento em cache de dados intermediários é desativado. O armazenamento em cache só deve ser ativado quando a imagem intermediária for reutilizada em um pedido diferente dentro de um período de tempo razoável. O gerenciamento de cache padrão do lado do servidor se aplica. Os dados são armazenados em cache em um formato sem perdas.
