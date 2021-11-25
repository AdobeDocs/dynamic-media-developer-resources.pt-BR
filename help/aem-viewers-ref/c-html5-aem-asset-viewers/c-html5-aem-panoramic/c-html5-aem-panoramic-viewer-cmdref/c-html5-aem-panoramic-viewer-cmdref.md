---
title: Referência de comando - Atributos de configuração
description: Documentação dos atributos de configuração para o Visualizador panorâmico.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: null
source-git-commit: 6118fac8a41abaf5db150820b982bec5bc45f0ff
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Documentação dos atributos de configuração para o Visualizador panorâmico.

Qualquer comando de configuração pode ser definido no URL ou usando `setParam()` e/ou `setParams()` Métodos da API. Qualquer atributo de configuração também pode ser especificado no registro de configuração do lado do servidor.

Alguns comandos de configuração podem ter o prefixo com o nome da classe ou o nome da instância do componente HTML5 SDK correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do contêiner do visualizador passado para `setContainerId()` Método da API. A documentação incluirá o prefixo opcional para esses comandos. Por exemplo, `vrrender` O comando será documentado da seguinte maneira:

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

O que significa que esse comando é usado da seguinte maneira:

* `vrrender` (sintaxe curta)
* `PanoramicView.vrrender` (qualificado com o nome da classe do componente)
* `cont_panoramicView.vrrender` (qualificado com a ID do componente, supondo que cont seja a ID do elemento do contêiner)


Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Consulte [Referência de comando comum a todos os visualizadores - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
