---
title: Referência de comando - Atributos de configuração
description: Documentação de atributos de configuração para o Flyout Viewer
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 15e7881f-ec4f-4e44-9833-1cf965800760
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Documentação de atributos de configuração para o Flyout Viewer

Você pode definir qualquer comando de configuração no URL. Ou, você pode usar `setParam()`, `setParams()`ou ambos os métodos da API. Você também pode especificar qualquer atributo de configuração no registro de configuração do lado do servidor.

Alguns comandos de configuração recebem o prefixo com o nome da classe ou o nome da instância do componente SDK do Visualizador correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do contêiner do visualizador passado para `setContainerId()` Método da API. A documentação inclui um prefixo opcional para esses comandos. Por exemplo, a variável `zoomfactor` O comando é documentado da seguinte maneira:

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

O comando é usado da seguinte maneira:

* `zoomfactor` (sintaxe curta)
* `FlyoutZoomView.zoomfactor` (qualificado com um nome de classe de componente)
* `cont_flyout.zoomfactor` (qualificado com a ID do componente, supondo que `cont` é a ID do elemento do contêiner)

Consulte também [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
