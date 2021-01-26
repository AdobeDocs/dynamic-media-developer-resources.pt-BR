---
description: Para aplicativos avançados, é possível usar o resultado de uma operação de renderização como uma imagem de material, assim como uma imagem obtida do Serviço de imagem.
seo-description: Para aplicativos avançados, é possível usar o resultado de uma operação de renderização como uma imagem de material, assim como uma imagem obtida do Serviço de imagem.
seo-title: Solicitações de renderização de imagem aninhada
solution: Experience Manager
title: Solicitações de renderização de imagem aninhada
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 12551bd5-ff5f-45d6-81e9-5ba0be47a425
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---


# Solicitações de renderização de imagem aninhada{#nested-image-rendering-requests}

Para aplicativos avançados, é possível usar o resultado de uma operação de renderização como uma imagem de material, assim como uma imagem obtida do Serviço de imagem.

Uma solicitação de renderização pode ser usada como uma imagem de material, especificando-a no comando `src=` da seguinte maneira:

` …&src=ir{ *[!DNL renderRequest]*}&…`

O token `ir` faz distinção entre maiúsculas e minúsculas.

A solicitação aninhada não deve incluir o caminho raiz de Renderização de imagem (normalmente `http:// *[!DNL server]*/ir/render/'`), mas pode incluir tokens de regras de pré-processamento.

Os seguintes comandos são ignorados quando especificados em solicitações aninhadas (no url de solicitação ou em `catalog::Modifier` ou `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

Também são ignorados `attribute::MaxPix` e `attribute::DefaultPix` do catálogo de materiais que se aplica à solicitação de renderização aninhada.

O resultado da imagem de uma solicitação IR aninhada pode ser armazenado em cache opcionalmente, incluindo `cache=on`. Por padrão, o cache de dados intermediários é desativado. O armazenamento em cache só deve ser ativado quando se espera que a imagem intermediária seja reutilizada em uma solicitação diferente dentro de um período de tempo razoável. O gerenciamento padrão de cache do lado do servidor se aplica. Os dados são armazenados em cache em um formato sem perdas.
