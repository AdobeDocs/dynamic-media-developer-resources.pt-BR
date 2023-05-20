---
title: Referência de comando - Atributos de configuração
description: Documentação de atributos de configuração do Visualizador do carrossel.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 71c2c973-d711-4d37-b778-381a7ec71527
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Documentação de atributos de configuração do Visualizador do carrossel.

Qualquer comando de configuração pode ser definido no URL ou usando `setParam()`ou `setParams()`, ou ambos, os métodos da API. Qualquer atributo de configuração também pode ser especificado no registro de configuração do lado do servidor.

Alguns comandos de configuração podem receber o nome da classe ou o nome da instância do componente SDK do visualizador correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do contêiner de visualização passado para `setContainerId()` método da API. A documentação inclui um prefixo opcional para esses comandos. Por exemplo, `zoomstep` está documentado da seguinte forma:

`[ZoomView.|<containerId>_carouselView].fmt`

Nesse caso, você pode usar este comando:

* `fmt` (sintaxe curta)
* `CarouselView.fmt` (qualificado com nome de classe de componente)
* `cont_carouselView.fmt` (qualificado com ID de componente, supondo `cont` é a ID do elemento do contêiner)

Consulte também [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
