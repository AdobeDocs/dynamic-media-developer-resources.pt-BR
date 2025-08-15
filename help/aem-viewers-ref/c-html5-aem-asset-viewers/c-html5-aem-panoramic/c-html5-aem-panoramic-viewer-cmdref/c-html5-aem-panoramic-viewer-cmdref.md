---
title: Referência de comando - Atributos de configuração
description: Documentação de atributos de configuração para o Visualizador Panorâmico.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Documentação de atributos de configuração para o Visualizador Panorâmico.

Qualquer comando de configuração pode ser definido na URL ou usando métodos de API `setParam()` e/ou `setParams()`. Qualquer atributo de configuração também pode ser especificado no registro de configuração do lado do servidor.

Alguns comandos de configuração podem receber o nome da classe ou o nome da instância do componente HTML5 SDK correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do contêiner de visualizador passado para o método de API `setContainerId()`. A documentação inclui prefixo opcional para esses comandos. Por exemplo, o comando `vrrender` está documentado da seguinte maneira:

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

O que significa que esse comando é usado da seguinte maneira:

* `vrrender` (sintaxe curta)
* `PanoramicView.vrrender` (qualificado com nome de classe de componente)
* `cont_panoramicView.vrrender` (qualificado com ID de componente, supondo que cont é a ID do elemento de contêiner)


Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Consulte [Referência de comando comum a todos os Visualizadores - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
