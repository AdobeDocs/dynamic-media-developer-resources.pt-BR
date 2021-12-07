---
title: Referência de comando - URL
description: Documentação de referência de comando para o visualizador de vídeo de recorte inteligente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# Referência de comando - URL{#command-reference-url}

Documentação de referência de comando para o visualizador de vídeo de recorte inteligente.

Você pode definir qualquer comando de configuração no URL. Ou você pode usar os métodos da API `setParam()`ou `setParams()`ou ambos para definir qualquer comando de configuração. Você também pode especificar qualquer atributo de configuração no registro de configuração do lado do servidor.

Você pode prefixar alguns comandos de configuração com o nome da classe ou o nome da instância do componente SDK do visualizador correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do contêiner do visualizador passado para `setContainerId()` Método da API. A documentação inclui prefixos opcionais para esses comandos. Por exemplo, `playback` está documentada da seguinte forma:

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

O que significa que esse comando é usado da seguinte maneira:

* `playback` (sintaxe curta)
* `SmartCropVideoPlayer.playback` (qualificado com o nome da classe do componente)
* `cont_smartCropVideoPlayer.playback` (qualificado com a ID do componente, supondo que `cont` é a ID do elemento do contêiner)

Consulte também [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

Consulte também [Referência de comando comum a todos os visualizadores - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
