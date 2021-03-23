---
description: Uma solicitação do Servidor de imagem (IS) pode ser usada como uma imagem material.
seo-description: Uma solicitação do Servidor de imagem (IS) pode ser usada como uma imagem material.
seo-title: Solicitações do servidor de imagem incorporado
solution: Experience Manager
title: Solicitações do servidor de imagem incorporado
uuid: dd72880d-8824-40b3-a5da-0f6ff4922939
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---


# Solicitações do servidor de imagem incorporado{#embedded-image-server-requests}

Uma solicitação do Servidor de imagem (IS) pode ser usada como uma imagem material.

Especifique a solicitação no comando `src=` da seguinte maneira:

` …&src=is( *[!DNL imageServingRequest]*)&…`

O token `is` diferencia maiúsculas de minúsculas.

A solicitação aninhada não deve incluir o caminho raiz do Serviço de imagem (normalmente [!DNL http:// *[!DNL server]*/is/image/&quot;]), mas pode incluir tokens de regras de pré-processamento.

Os seguintes comandos IS são ignorados quando especificados em solicitações aninhadas (no URL da solicitação ou em `catalog::Modifier` ou `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

Também são ignoradas `attribute::MaxPix` e `attribute::DefaultPix` do catálogo de imagem que se aplica à solicitação IS incorporada.

Se a imagem resultante da solicitação aninhada incluir dados de máscara (alfa), ela sempre será passada para o material. Use uma camada de imagem de fundo de cor sólida para evitar alfa indesejado.

O resultado da imagem de uma solicitação IS incorporada pode ser armazenado em cache opcionalmente, incluindo `cache=on`. Por padrão, o armazenamento em cache de dados intermediários é desativado. O armazenamento em cache só deve ser ativado quando se espera que a imagem intermediária seja reutilizada num pedido diferente dentro de um período de tempo razoável. O gerenciamento de cache padrão do lado do servidor se aplica. Os dados são armazenados em cache em um formato sem perdas.
