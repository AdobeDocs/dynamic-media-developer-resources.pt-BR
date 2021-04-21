---
description: Documentação dos atributos de configuração do Visualizador de zoom.
solution: Experience Manager
title: Referência de comando - Atributos de configuração
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---


# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Documentação dos atributos de configuração do Visualizador de zoom.

Qualquer comando de configuração pode ser definido no URL ou usando `setParam()`, ou `setParams()`, ou ambos os métodos de API. Qualquer atributo de configuração também pode ser especificado no registro de configuração do lado do servidor.

Alguns comandos de configuração podem ter o prefixo com o nome da classe ou o nome da instância do componente SDK do Visualizador correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do contêiner do visualizador passado para o método de API `setContainerId()` . A documentação inclui um prefixo opcional para esses comandos. Por exemplo, o comando `zoomstep` está documentado da seguinte maneira:

`[ZoomView.|<containerId>_zoomView].zoomstep`

o que significa que você pode usar este comando como:

* `zoomstep` (sintaxe curta)
* `ZoomView.zoomstep` (qualificado com o nome da classe do componente)
* `cont_zoomView.zoomstep` (qualificado com a ID do componente, supondo que  `cont` seja a ID do elemento do contêiner)

Consulte também [Referência de comando comum para todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
