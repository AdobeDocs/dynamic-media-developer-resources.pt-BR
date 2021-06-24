---
description: Documentação de atributos de configuração para o Visualizador de catálogo eletrônico.
solution: Experience Manager
title: Referência de comando - Atributos de configuração
feature: Dynamic Media Classic,Visualizadores,SDK/API,Pesquisa de catálogo eletrônico
role: Developer,Business Practitioner
exl-id: e8ce40c9-d1c0-454f-b8fa-ba19e3fe2091
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---

# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Documentação de atributos de configuração para o Visualizador de catálogo eletrônico.

Qualquer comando de configuração pode ser definido no URL ou usando `setParam()`, ou `setParams()`, ou ambos os métodos de API. Você também pode especificar qualquer atributo de configuração especificado no registro de configuração do lado do servidor.

Para alguns comandos de configuração, você pode prefixá-los com o nome da classe ou da instância do componente SDK do visualizador correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do contêiner do visualizador passado para o método de API `setContainerId()` . A documentação inclui o prefixo opcional para esses comandos. Por exemplo, o comando `zoomstep` está documentado da seguinte maneira:

`[PageView.|<containerId>_pageView].zoomstep`

o que significa que você pode usar este comando como:

* `zoomstep` (sintaxe curta)
* `PageView.zoomstep` (qualificado com o nome da classe do componente)
* `cont_pageView.zoomstep` (qualificado com a ID do componente, supondo que  `cont` seja a ID do elemento do contêiner)

Consulte também [Referência de comando comum para todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
