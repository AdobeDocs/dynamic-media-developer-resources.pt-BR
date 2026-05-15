---
title: Referência de comando - Atributos de configuração
description: Documentação de atributos de configuração para o Visualizador Panorâmico.
solution: Experience Manager
role: Developer,User
autotag-review: '2026-05-13T22:15:11.019Z'
TQID: 'https://experienceleague.adobe.com/-6kskMStr-k7aFwy9GpQE-wjq4iAgwuEqzP2H1BWk2U'
product_v2:
  - id: beaff0dd-a904-4c6b-8290-b527cd877d75
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 149
ht-degree: 0%

---

# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

<!--
feature: Dynamic Media Classic,Viewers,SDK/API
-->

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
