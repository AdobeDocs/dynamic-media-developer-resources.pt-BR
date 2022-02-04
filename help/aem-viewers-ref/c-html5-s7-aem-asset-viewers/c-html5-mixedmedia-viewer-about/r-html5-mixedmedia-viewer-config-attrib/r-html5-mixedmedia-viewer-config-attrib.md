---
title: Referência de comando - Atributos de configuração
description: Documentação dos atributos de configuração do Visualizador de mídia mista.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: aa750941-0a2e-4591-bdff-5e71ecc342aa
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Documentação dos atributos de configuração do Visualizador de mídia mista.

Qualquer comando de configuração pode ser definido no URL ou usando `setParam()`ou `setParams()`, ou ambos, os métodos da API. Qualquer atributo de configuração também pode ser especificado no registro de configuração do lado do servidor.

Alguns comandos de configuração podem ter o prefixo com o nome da classe ou o nome da instância do componente SDK do Visualizador correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do contêiner do visualizador passado para `setContainerId()` Método da API. A documentação inclui um prefixo opcional para esses comandos. Por exemplo, `zoomstep` O comando é documentado da seguinte maneira:

`[ZoomView.|<containerId>_zoomView].zoomstep`

Isso significa que você pode usar esse comando da seguinte maneira

* `zoomstep` (sintaxe curta)
* `ZoomView.zoomstep` (qualificado com o nome da classe do componente)
* `cont_zoomView.zoomstep` (qualificado com a ID do componente, considerando `cont` é a ID do elemento do contêiner)

Consulte também [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
