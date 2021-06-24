---
description: Documentação dos atributos de configuração para o visualizador de vídeo.
solution: Experience Manager
title: Referência de comando - Atributos de configuração
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Developer,Business Practitioner
exl-id: 5992e5cd-7783-408e-a23f-fdcc3a3d6b69
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Documentação dos atributos de configuração para o visualizador de vídeo.

Você pode definir qualquer comando de configuração no URL. Ou você pode usar os métodos da API `setParam()`, ou `setParams()`, ou ambos para definir qualquer comando de configuração. Você também pode especificar qualquer atributo de configuração no registro de configuração do lado do servidor.

Você pode prefixar alguns comandos de configuração com o nome da classe ou o nome da instância do componente SDK do visualizador correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do contêiner do visualizador passado para o método de API `setContainerId()` . A documentação inclui prefixos opcionais para esses comandos. Por exemplo, `playback` está documentado da seguinte maneira:

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

o que significa que esse comando é usado da seguinte maneira:

* `playback` (sintaxe curta)
* `VideoPlayer.playback` (qualificado com o nome da classe do componente)
* `cont_videoPlayer.playback` (qualificado com a ID do componente, supondo que  `cont` seja a ID do elemento do contêiner)

Consulte [Referência de comando comum para todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Consulte [Referência de comando comum para todos os visualizadores - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
