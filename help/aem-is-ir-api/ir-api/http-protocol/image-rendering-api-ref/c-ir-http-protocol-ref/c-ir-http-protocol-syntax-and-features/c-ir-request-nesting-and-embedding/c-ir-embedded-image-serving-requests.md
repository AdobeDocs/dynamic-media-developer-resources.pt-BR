---
title: Solicitações do servidor de imagens incorporadas
description: Uma solicitação do Servidor de imagens (IS) pode ser usada como uma imagem do material.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# Solicitações do servidor de imagens incorporadas{#embedded-image-server-requests}

Uma solicitação do Servidor de imagens (IS) pode ser usada como uma imagem do material.

Especifique a solicitação no `src=` comando da seguinte maneira:

` …&src=is( *[!DNL imageServingRequest]*)&…`

A variável `is` O token diferencia maiúsculas e minúsculas.

A solicitação aninhada não deve incluir o caminho raiz do Servidor de imagens (normalmente [!DNL http:// *[!DNL server]*/is/image/"]), mas pode incluir tokens de regra de pré-processamento.

Os seguintes comandos IS são ignorados quando especificados em solicitações aninhadas (no URL da solicitação ou no `catalog::Modifier` ou `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

Também são ignoradas `attribute::MaxPix` e `attribute::DefaultPix` do catálogo de imagens que se aplica à solicitação IS incorporada.

Se a imagem resultante da solicitação aninhada incluir dados de máscara (alfa), ela será sempre passada para o material. Use uma camada de imagem de plano de fundo de cor sólida para evitar alfa indesejado.

O resultado da imagem de uma solicitação IS incorporada pode ser armazenado em cache opcionalmente incluindo `cache=on`. Por padrão, o armazenamento em cache de dados intermediários está desativado. O armazenamento em cache só deve ser ativado quando a imagem intermediária for reutilizada em uma solicitação diferente em um período de tempo razoável. O gerenciamento padrão de cache do lado do servidor se aplica. Os dados são armazenados em cache em um formato sem perdas.
