---
title: Solicitações de renderização de imagem aninhada
description: Para aplicativos avançados, é possível usar o resultado de uma operação de renderização como uma imagem material, como uma imagem obtida do Serviço de imagem.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# Solicitações de renderização de imagem aninhada{#nested-image-rendering-requests}

Para aplicativos avançados, é possível usar o resultado de uma operação de renderização como uma imagem material, como uma imagem obtida do Serviço de imagem.

Uma solicitação de renderização pode ser usada como uma imagem de material ao especificá-la na variável `src=` comando como segue:

` …&src=ir{ *[!DNL renderRequest]*}&…`

O `ir` O token diferencia maiúsculas de minúsculas.

A solicitação aninhada não deve incluir o caminho raiz da Renderização de imagem (normalmente `http:// *[!DNL server]*/ir/render/'`), mas pode incluir tokens de regras de pré-processamento.

Os comandos a seguir são ignorados quando especificados em solicitações aninhadas (no url da solicitação ou em `catalog::Modifier` ou `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

Também são ignoradas `attribute::MaxPix` e `attribute::DefaultPix` do catálogo de materiais que se aplica à solicitação de renderização aninhada.

O resultado da imagem de uma solicitação IR aninhada pode ser armazenado em cache opcionalmente, incluindo `cache=on`. Por padrão, o armazenamento em cache de dados intermediários é desativado. O armazenamento em cache só deve ser ativado quando a imagem intermediária for reutilizada em um pedido diferente dentro de um período de tempo razoável. O gerenciamento de cache padrão do lado do servidor se aplica. Os dados são armazenados em cache em um formato sem perdas.
