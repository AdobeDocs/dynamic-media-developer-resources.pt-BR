---
description: Documentação de referência de comando para o Visualizador de vídeo.
seo-description: Documentação de referência de comando para o Visualizador de vídeo.
seo-title: Referência de comando - URL
solution: Experience Manager
title: Referência de comando - URL
topic: Dynamic media
uuid: 4f9e4a79-6865-4e41-b30b-84ff2c6f6045
translation-type: tm+mt
source-git-commit: 3266e8682711dac379a09a0e992d33b8ffc7b5a4

---


# Referência de comando - URL{#command-reference-url}

Documentação de referência de comando para o Visualizador de vídeo.

É possível definir qualquer comando de configuração no URL. Ou você pode usar os métodos da API `setParam()`, ou `setParams()`, ou ambos, para definir qualquer comando de configuração. Você também pode especificar qualquer atributo de configuração no registro de configuração do lado do servidor.

Você pode prefixar alguns comandos de configuração com o nome da classe ou da instância do componente SDK do visualizador correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do container do visualizador passado para o método `setContainerId()` API. A documentação inclui prefixos opcionais para esses comandos. Por exemplo, `playback` é documentado da seguinte forma:

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

o que significa que esse comando é usado da seguinte maneira:

* `playback` (sintaxe curta)
* `VideoPlayer.playback` (qualificado com o nome da classe do componente)
* `cont_videoPlayer.playback` (qualificado com a ID do componente, supondo que `cont` seja a ID do elemento do container)

Consulte também Referência de [comando comum para todos os visualizadores - Atributos](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)de configuração.

Consulte também Referência de [comando comum para todos os visualizadores - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
