---
title: Solicitações de renderização de imagem aninhada
description: Para aplicativos avançados, é possível usar o resultado de uma operação de renderização como uma imagem do material, como uma imagem obtida no Servidor de imagens.
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

Para aplicativos avançados, é possível usar o resultado de uma operação de renderização como uma imagem do material, como uma imagem obtida no Servidor de imagens.

Uma solicitação de renderização pode ser usada como uma imagem do material especificando-a no campo `src=` comando da seguinte maneira:

` …&src=ir{ *[!DNL renderRequest]*}&…`

A variável `ir` O token diferencia maiúsculas e minúsculas.

A solicitação aninhada não deve incluir o caminho raiz de Renderização de imagem (normalmente `http:// *[!DNL server]*/ir/render/'`), mas pode incluir tokens de regra de pré-processamento.

Os seguintes comandos são ignorados quando especificados em solicitações aninhadas (no url da solicitação ou no `catalog::Modifier` ou `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

Também são ignoradas `attribute::MaxPix` e `attribute::DefaultPix` do catálogo de materiais que se aplica à solicitação de renderização aninhada.

O resultado de imagem de uma solicitação IR aninhada pode ser armazenado em cache opcionalmente incluindo `cache=on`. Por padrão, o armazenamento em cache de dados intermediários está desativado. O armazenamento em cache só deve ser ativado quando a imagem intermediária for reutilizada em uma solicitação diferente em um período de tempo razoável. O gerenciamento padrão de cache do lado do servidor se aplica. Os dados são armazenados em cache em um formato sem perdas.
