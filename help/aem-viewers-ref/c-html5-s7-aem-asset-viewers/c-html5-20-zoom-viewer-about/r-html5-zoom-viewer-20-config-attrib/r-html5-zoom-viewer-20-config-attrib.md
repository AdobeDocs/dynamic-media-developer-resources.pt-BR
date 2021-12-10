---
title: Referência de comando - Atributos de configuração
description: Documentação dos atributos de configuração do Visualizador de zoom.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 03982627-9298-4032-a15a-a5afe4ec1fb5
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Documentação dos atributos de configuração do Visualizador de zoom.

Qualquer comando de configuração pode ser definido no URL ou usando `setParam()`ou `setParams()`, ou ambos, os métodos da API. Qualquer atributo de configuração também pode ser especificado no registro de configuração do lado do servidor.

Alguns comandos de configuração podem ter o prefixo com o nome da classe ou o nome da instância do componente SDK do Visualizador correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do contêiner do visualizador passado para `setContainerId()` Método da API. A documentação inclui um prefixo opcional para esses comandos. Por exemplo, `zoomstep` O comando é documentado da seguinte maneira:

`[ZoomView.|<containerId>_zoomView].zoomstep`

Isso significa que você pode usar o comando como

* `zoomstep` (sintaxe curta)
* `ZoomView.zoomstep` (qualificado com o nome da classe do componente)
* `cont_zoomView.zoomstep` (qualificado com a ID do componente, considerando `cont` é a ID do elemento do contêiner)

Consulte também [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
