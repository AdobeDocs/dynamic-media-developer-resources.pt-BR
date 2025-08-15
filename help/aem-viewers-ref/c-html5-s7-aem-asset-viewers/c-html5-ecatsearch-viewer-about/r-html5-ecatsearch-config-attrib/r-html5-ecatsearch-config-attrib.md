---
description: Documentação de atributos de configuração do eCatalog Viewer.
solution: Experience Manager
title: Referência de comando - Atributos de configuração
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e8ce40c9-d1c0-454f-b8fa-ba19e3fe2091
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Documentação de atributos de configuração do eCatalog Viewer.

Qualquer comando de configuração pode ser definido na URL ou usando `setParam()`, `setParams()` ou ambos os métodos de API. Você também pode especificar qualquer atributo de configuração especificado no registro de configuração do lado do servidor.

Para alguns comandos de configuração, você pode adicionar prefixos com o nome da classe ou da instância do componente SDK do visualizador correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do contêiner de visualizador passado para o método de API `setContainerId()`. A documentação inclui prefixo opcional para esses comandos. Por exemplo, o comando `zoomstep` está documentado da seguinte maneira:

`[PageView.|<containerId>_pageView].zoomstep`

o que significa que você pode usar esse comando como:

* `zoomstep` (sintaxe curta)
* `PageView.zoomstep` (qualificado com nome de classe de componente)
* `cont_pageView.zoomstep` (qualificado com ID de componente, supondo que `cont` seja a ID do elemento de contêiner)

Consulte também [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
