---
description: Documentação de atributos de configuração para o Flyout Viewer
seo-description: Documentação de atributos de configuração para o Flyout Viewer
seo-title: Referência de comando - Atributos de configuração
solution: Experience Manager
title: Referência de comando - Atributos de configuração
topic: Dynamic Media
uuid: 0813c334-37b7-43af-b39d-bec66658ad58
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---


# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Documentação de atributos de configuração para o Flyout Viewer

É possível definir qualquer comando de configuração no URL. Ou você pode usar `setParam()`, `setParams()` ou ambos os métodos de API. Você também pode especificar qualquer atributo de configuração no registro de configuração do servidor.

Alguns comandos de configuração recebem o prefixo nome da classe ou da instância do componente SDK do visualizador correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do container do visualizador passado para o método da API `setContainerId()`. A documentação inclui um prefixo opcional para esses comandos. Por exemplo, o comando `zoomfactor` é documentado da seguinte maneira:

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

O comando é usado da seguinte maneira:

* `zoomfactor` (sintaxe curta)
* `FlyoutZoomView.zoomfactor` (qualificado com um nome de classe de componente)
* `cont_flyout.zoomfactor` (qualificado com a ID do componente, supondo que essa  `cont` seja a ID do elemento do container)

Consulte também [Referência de comando comum para todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
