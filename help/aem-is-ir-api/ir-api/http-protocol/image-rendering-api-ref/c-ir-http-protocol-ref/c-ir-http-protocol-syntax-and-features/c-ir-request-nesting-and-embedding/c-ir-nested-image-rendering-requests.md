---
description: Para aplicativos avançados, é possível usar o resultado de uma operação de renderização como uma imagem material, como uma imagem obtida do Serviço de imagem.
solution: Experience Manager
title: Solicitações de renderização de imagem aninhada
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# Solicitações de renderização de imagem aninhada{#nested-image-rendering-requests}

Para aplicativos avançados, é possível usar o resultado de uma operação de renderização como uma imagem material, como uma imagem obtida do Serviço de imagem.

Uma solicitação de renderização pode ser usada como uma imagem de material, especificando-a no comando `src=` da seguinte maneira:

` …&src=ir{ *[!DNL renderRequest]*}&…`

O token `ir` diferencia maiúsculas de minúsculas.

A solicitação aninhada não deve incluir o caminho raiz da Renderização de imagem (normalmente `http:// *[!DNL server]*/ir/render/'`), mas pode incluir tokens de regras de pré-processamento.

Os seguintes comandos são ignorados quando especificados em solicitações aninhadas (no url da solicitação ou em `catalog::Modifier` ou `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

Também são ignoradas `attribute::MaxPix` e `attribute::DefaultPix` do catálogo de materiais que se aplica à solicitação de renderização aninhada.

O resultado da imagem de uma solicitação IR aninhada pode ser armazenado em cache opcionalmente, incluindo `cache=on`. Por padrão, o armazenamento em cache de dados intermediários é desativado. O armazenamento em cache só deve ser ativado quando se espera que a imagem intermediária seja reutilizada num pedido diferente dentro de um período de tempo razoável. O gerenciamento de cache padrão do lado do servidor se aplica. Os dados são armazenados em cache em um formato sem perdas.
