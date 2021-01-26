---
description: Uma solicitação do Servidor de imagens (IS) pode ser usada como uma imagem de material.
seo-description: Uma solicitação do Servidor de imagens (IS) pode ser usada como uma imagem de material.
seo-title: Solicitações do Servidor de imagens incorporado
solution: Experience Manager
title: Solicitações do Servidor de imagens incorporado
topic: Dynamic Media Image Serving - Image Rendering API
uuid: dd72880d-8824-40b3-a5da-0f6ff4922939
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---


# Solicitações do Servidor de Imagens Incorporado{#embedded-image-server-requests}

Uma solicitação do Servidor de imagens (IS) pode ser usada como uma imagem de material.

Especifique a solicitação no comando `src=` da seguinte maneira:

` …&src=is( *[!DNL imageServingRequest]*)&…`

O token `is` faz distinção entre maiúsculas e minúsculas.

A solicitação aninhada não deve incluir o caminho raiz do Servidor de imagens (normalmente [!DNL http:// *[!DNL server]*/is/image/&quot;]), mas pode incluir tokens de regras de pré-processamento.

Os seguintes comandos IS são ignorados quando especificados em solicitações aninhadas (no URL da solicitação ou em `catalog::Modifier` ou `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

Também são ignorados `attribute::MaxPix` e `attribute::DefaultPix` do catálogo de imagens que se aplica à solicitação IS incorporada.

Se a imagem resultante da solicitação aninhada incluir dados de máscara (alfa), ela sempre será passada para o material. Use uma camada de imagem de plano de fundo de cor sólida para evitar alfa indesejado.

O resultado da imagem de uma solicitação IS incorporada pode ser armazenado em cache opcionalmente, incluindo `cache=on`. Por padrão, o cache de dados intermediários é desativado. O armazenamento em cache só deve ser ativado quando se espera que a imagem intermediária seja reutilizada em uma solicitação diferente dentro de um período de tempo razoável. O gerenciamento padrão de cache do lado do servidor se aplica. Os dados são armazenados em cache em um formato sem perdas.
