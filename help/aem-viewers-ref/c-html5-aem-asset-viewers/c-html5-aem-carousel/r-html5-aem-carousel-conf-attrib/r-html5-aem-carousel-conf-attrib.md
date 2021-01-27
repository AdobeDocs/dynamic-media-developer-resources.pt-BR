---
description: Documentação de atributos de configuração para o Visualizador do carrossel.
seo-description: Documentação de atributos de configuração para o Visualizador do carrossel.
seo-title: Referência de comando - Atributos de configuração
solution: Experience Manager
title: Referência de comando - Atributos de configuração
topic: Dynamic Media
uuid: 036af728-ab00-4db3-98cf-d16f1bffa064
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---


# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Documentação de atributos de configuração para o Visualizador do carrossel.

Qualquer comando de configuração pode ser definido no URL ou usando `setParam()`, `setParams()` ou ambos os métodos de API. Qualquer atributo de configuração também pode ser especificado no registro de configuração do lado do servidor.

Alguns comandos de configuração podem receber o prefixo nome da classe ou da instância do componente SDK do visualizador correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do container do visualizador passado para o método da API `setContainerId()`. A documentação inclui um prefixo opcional para esses comandos. Por exemplo, o comando `zoomstep` está documentado da seguinte maneira:

`[ZoomView.|<containerId>_carouselView].fmt`

o que significa que você pode usar esse comando como:

* `fmt` (sintaxe curta)
* `CarouselView.fmt` (qualificado com o nome da classe do componente)
* `cont_carouselView.fmt` (qualificado com a ID do componente, supondo que  `cont` seja a ID do elemento do container)

Consulte também [Referência de comando comum para todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
