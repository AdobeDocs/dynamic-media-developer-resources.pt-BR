---
title: Solicitações de renderização de imagem aninhada
description: Para aplicativos avançados, é possível usar o resultado de uma operação de renderização como uma imagem do material, como uma imagem obtida no Servidor de imagens.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
TQID: 'https://experienceleague.adobe.com/Fqiu-HsaRtrWMjBQudUBzr1iu3WLg7173Kf-71ikejI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 0%

---

# Solicitações de renderização de imagem aninhada{#nested-image-rendering-requests}

Para aplicativos avançados, é possível usar o resultado de uma operação de renderização como uma imagem do material, como uma imagem obtida no Servidor de imagens.

Uma solicitação de renderização pode ser usada como uma imagem do material especificando-a no comando `src=` da seguinte maneira:

` …&src=ir{ *[!DNL renderRequest]*}&…`

O token `ir` diferencia maiúsculas de minúsculas.

A solicitação aninhada não deve incluir o caminho raiz de Renderização de Imagem (normalmente `http:// *[!DNL server]*/ir/render/'`), mas pode incluir tokens de regra de pré-processamento.

Os seguintes comandos são ignorados quando especificados em solicitações aninhadas (na url de solicitação ou em `catalog::Modifier` ou `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

Também são ignorados `attribute::MaxPix` e `attribute::DefaultPix` do catálogo de materiais que se aplica à solicitação de renderização aninhada.

O resultado da imagem de uma solicitação de IR aninhada pode ser armazenado em cache opcionalmente incluindo `cache=on`. Por padrão, o armazenamento em cache de dados intermediários está desativado. O armazenamento em cache só deve ser ativado quando a imagem intermediária for reutilizada em uma solicitação diferente em um período de tempo razoável. O gerenciamento padrão de cache do lado do servidor se aplica. Os dados são armazenados em cache em um formato sem perdas.
