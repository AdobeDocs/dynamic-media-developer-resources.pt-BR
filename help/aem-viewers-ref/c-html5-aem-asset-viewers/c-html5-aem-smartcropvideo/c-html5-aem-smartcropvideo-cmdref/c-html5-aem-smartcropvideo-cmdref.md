---
title: Referência de comando - Atributos de configuração
description: Documentação de atributos de configuração para o Visualizador de vídeo de recorte inteligente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
mini-toc-levels: 3
exl-id: 698c03b1-bec0-44bf-9c79-c66e0192344a
source-git-commit: eaf59166fcc1ff8ec5a2e846ef0eb180c8cbdd5a
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Documentação de atributos de configuração para o Visualizador de vídeo de recorte inteligente.

Você pode definir qualquer comando de configuração no URL. Ou você pode usar os métodos de API `setParam()`, `setParams()` ou ambos para definir qualquer comando de configuração. Você também pode especificar qualquer atributo de configuração no registro de configuração do lado do servidor.

Você pode adicionar prefixos a alguns comandos de configuração com o nome da classe ou da instância do componente SDK do visualizador correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do contêiner de visualizador passado para o método de API `setContainerId()`. A documentação inclui prefixos opcionais para esses comandos. Por exemplo, `playback` é documentado da seguinte maneira:

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

O que significa que esse comando é usado da seguinte maneira:

* `playback` (sintaxe curta)
* `SmartCropVideoPlayer.playback` (qualificado com nome de classe de componente)
* `cont_videoPlayer.playback` (qualificado com ID de componente, supondo que `cont` seja a ID do elemento de contêiner)

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Consulte [Referência de comando comum a todos os Visualizadores - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
