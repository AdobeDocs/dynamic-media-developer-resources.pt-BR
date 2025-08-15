---
title: Referência de comando - Atributos de configuração
description: Documentação de atributos de configuração para o Visualizador de mídia mista.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: aa750941-0a2e-4591-bdff-5e71ecc342aa
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Documentação de atributos de configuração para o Visualizador de mídia mista.

Qualquer comando de configuração pode ser definido na URL ou usando `setParam()`, `setParams()` ou ambos os métodos de API. Qualquer atributo de configuração também pode ser especificado no registro de configuração do lado do servidor.

Alguns comandos de configuração podem receber o nome da classe ou o nome da instância do componente SDK do visualizador correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do contêiner de visualizador passado para o método de API `setContainerId()`. A documentação inclui um prefixo opcional para esses comandos. Por exemplo, o comando `zoomstep` está documentado da seguinte maneira:

`[ZoomView.|<containerId>_zoomView].zoomstep`

O que significa que você pode usar esse comando da seguinte maneira

* `zoomstep` (sintaxe curta)
* `ZoomView.zoomstep` (qualificado com nome de classe de componente)
* `cont_zoomView.zoomstep` (qualificado com ID de componente, supondo que `cont` seja a ID do elemento de contêiner)

Consulte também [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
