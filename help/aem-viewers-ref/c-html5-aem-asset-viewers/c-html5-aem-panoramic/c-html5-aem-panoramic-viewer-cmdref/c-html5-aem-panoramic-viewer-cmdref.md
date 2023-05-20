---
title: Referência de comando - Atributos de configuração
description: Documentação de atributos de configuração para o Visualizador Panorâmico.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Documentação de atributos de configuração para o Visualizador Panorâmico.

Qualquer comando de configuração pode ser definido no URL ou usando `setParam()` e/ou `setParams()` Métodos da API. Qualquer atributo de configuração também pode ser especificado no registro de configuração do lado do servidor.

Alguns comandos de configuração podem receber o nome da classe ou o nome da instância do componente SDK HTML5 correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do contêiner de visualização passado para `setContainerId()` método da API. A documentação incluirá o prefixo opcional para esses comandos. Por exemplo, `vrrender` está documentado da seguinte forma:

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

O que significa que esse comando é usado da seguinte maneira:

* `vrrender` (sintaxe curta)
* `PanoramicView.vrrender` (qualificado com nome de classe de componente)
* `cont_panoramicView.vrrender` (qualificado com ID de componente, supondo que cont seja a ID do elemento de contêiner)


Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Consulte [Referência de comando comum a todos os visualizadores - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
