---
title: Referência de comando - URL
description: Documentação de referência de comandos para o Visualizador de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 1ed78e0d-9b93-4c66-b558-fac15c51e944
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---

# Referência de comando - URL{#command-reference-url}

Documentação de referência de comandos para o Visualizador de vídeo.

Você pode definir qualquer comando de configuração no URL. Ou você pode usar os métodos de API `setParam()`, `setParams()` ou ambos para definir qualquer comando de configuração. Você também pode especificar qualquer atributo de configuração no registro de configuração do lado do servidor.

Você pode adicionar prefixos a alguns comandos de configuração com o nome da classe ou da instância do componente SDK do visualizador correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do contêiner de visualizador passado para o método de API `setContainerId()`. A documentação inclui prefixos opcionais para esses comandos. Por exemplo, `playback` é documentado da seguinte maneira:

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

O que significa que esse comando é usado da seguinte maneira

* `playback` (sintaxe curta)
* `VideoPlayer.playback` (qualificado com nome de classe de componente)
* `cont_videoPlayer.playback` (qualificado com ID de componente, supondo que `cont` seja a ID do elemento de contêiner)

Consulte também [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

Consulte também [Referência de comando comum a todos os Visualizadores - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
