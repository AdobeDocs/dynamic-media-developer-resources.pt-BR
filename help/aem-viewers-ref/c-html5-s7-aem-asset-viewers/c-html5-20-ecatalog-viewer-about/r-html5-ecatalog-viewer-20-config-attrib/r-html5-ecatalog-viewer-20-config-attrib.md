---
title: Referência de comando - Atributos de configuração
description: Documentação de atributos de configuração para o Visualizador de catálogo eletrônico.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d15061db-8941-44aa-b90d-598c1ce58a67
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Documentação de atributos de configuração para o Visualizador de catálogo eletrônico.

Qualquer comando de configuração pode ser definido no URL ou usando `setParam()`ou `setParams()`, ou ambos, os métodos da API. Você também pode especificar qualquer atributo de configuração especificado no registro de configuração do lado do servidor.

Para alguns comandos de configuração, você pode prefixá-los com o nome da classe ou da instância do componente SDK do visualizador correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do contêiner do visualizador passado para `setContainerId()` Método da API. A documentação inclui o prefixo opcional para esses comandos. Por exemplo, `zoomstep` O comando é documentado da seguinte maneira:

`[PageView.|<containerId>_pageView].zoomstep`

O que significa que você pode usar esse comando como

* `zoomstep` (sintaxe curta)
* `PageView.zoomstep` (qualificado com o nome da classe do componente)
* `cont_pageView.zoomstep` (qualificado com a ID do componente, considerando `cont` é a ID do elemento do contêiner)

Consulte também [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
