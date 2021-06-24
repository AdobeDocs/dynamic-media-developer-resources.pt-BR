---
description: Documentação de atributos de configuração para o Flyout Viewer
solution: Experience Manager
title: Referência de comando - Atributos de configuração
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom em linha
role: Developer,Business Practitioner
exl-id: 15e7881f-ec4f-4e44-9833-1cf965800760
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Documentação de atributos de configuração para o Flyout Viewer

Você pode definir qualquer comando de configuração no URL. Ou você pode usar `setParam()`, `setParams()` ou ambos os métodos de API. Você também pode especificar qualquer atributo de configuração no registro de configuração do lado do servidor.

Alguns comandos de configuração recebem o prefixo com o nome da classe ou o nome da instância do componente SDK do Visualizador correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do contêiner do visualizador passado para o método de API `setContainerId()` . A documentação inclui um prefixo opcional para esses comandos. Por exemplo, o comando `zoomfactor` é documentado da seguinte maneira:

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

O comando é usado da seguinte maneira:

* `zoomfactor` (sintaxe curta)
* `FlyoutZoomView.zoomfactor` (qualificado com um nome de classe de componente)
* `cont_flyout.zoomfactor` (qualificado com a ID do componente, supondo que  `cont` seja a ID do elemento do contêiner)

Consulte também [Referência de comando comum para todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
