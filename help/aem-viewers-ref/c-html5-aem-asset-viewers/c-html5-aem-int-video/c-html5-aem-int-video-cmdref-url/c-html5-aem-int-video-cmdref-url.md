---
title: Referência de comando - URL
description: Documentação de referência de comandos do Interative Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e0a9e269-4826-4518-9222-6a833d11746b
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# Referência de comando - URL{#command-reference-url}

Documentação de referência de comandos do Interative Video Viewer.

Você pode definir qualquer comando de configuração no URL. Ou você pode usar os métodos da API `setParam()`ou `setParams()`, ou ambos para definir qualquer comando de configuração. Você também pode especificar qualquer atributo de configuração no registro de configuração do lado do servidor.

Você pode adicionar prefixos a alguns comandos de configuração com o nome da classe ou o nome da instância do componente do SDK do visualizador correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do contêiner de visualização passado para `setContainerId()` método da API. A documentação inclui prefixos opcionais para esses comandos. Por exemplo, `playback` está documentado da seguinte forma:

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

O que significa que esse comando é usado da seguinte maneira

* `playback` (sintaxe curta)
* `VideoPlayer.playback` (qualificado com nome de classe de componente)
* `cont_videoPlayer.playback` (qualificado com ID de componente, supondo que `cont` é a ID do elemento do contêiner)

Consulte também [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

Consulte também [Referência de comando comum a todos os visualizadores - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
