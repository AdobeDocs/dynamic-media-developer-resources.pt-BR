---
title: Solicitações do servidor de imagens incorporadas
description: Uma solicitação do Servidor de imagens (IS) pode ser usada como uma imagem do material.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
TQID: 'https://experienceleague.adobe.com/dt-baBh9jAyJdjqopFR3AoqRvz5zqLzi8B3SnE04xEs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 0%

---

# Solicitações do servidor de imagens incorporadas{#embedded-image-server-requests}

Uma solicitação do Servidor de imagens (IS) pode ser usada como uma imagem do material.

Especifique a solicitação no comando `src=` da seguinte maneira:

` …&src=is( *[!DNL imageServingRequest]*)&…`

O token `is` diferencia maiúsculas de minúsculas.

A solicitação aninhada não deve incluir o caminho raiz do Servidor de Imagens (normalmente  [!DNL http:// *[!DNL server]*/is/image/"]), mas pode incluir tokens de regra de pré-processamento.

Os seguintes comandos IS são ignorados quando especificados em solicitações aninhadas (na URL da solicitação ou em `catalog::Modifier` ou `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

Também são ignorados `attribute::MaxPix` e `attribute::DefaultPix` do catálogo de imagens que se aplica à solicitação IS incorporada.

Se a imagem resultante da solicitação aninhada incluir dados de máscara (alfa), ela será sempre passada para o material. Use uma camada de imagem de plano de fundo de cor sólida para evitar alfa indesejado.

O resultado da imagem de uma solicitação IS inserida pode ser armazenado em cache opcionalmente incluindo `cache=on`. Por padrão, o armazenamento em cache de dados intermediários está desativado. O armazenamento em cache só deve ser ativado quando a imagem intermediária for reutilizada em uma solicitação diferente em um período de tempo razoável. O gerenciamento padrão de cache do lado do servidor se aplica. Os dados são armazenados em cache em um formato sem perdas.

