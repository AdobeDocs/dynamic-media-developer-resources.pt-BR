---
description: Documentação de atributos de configuração para o Visualizador de vídeo.
seo-description: Documentação de atributos de configuração para o Visualizador de vídeo.
seo-title: Referência de comando - Atributos de configuração
solution: Experience Manager
title: Referência de comando - Atributos de configuração
topic: Dynamic media
uuid: 837cf230-f7dd-4010-a299-c3267d11e200
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Documentação de atributos de configuração para o Visualizador de vídeo.

É possível definir qualquer comando de configuração no URL. Ou você pode usar os métodos da API `setParam()`, ou `setParams()`, ou ambos, para definir qualquer comando de configuração. Você também pode especificar qualquer atributo de configuração no registro de configuração do lado do servidor.

Você pode prefixar alguns comandos de configuração com o nome da classe ou da instância do componente SDK do visualizador correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do container do visualizador passado para o método `setContainerId()` API. A documentação inclui prefixos opcionais para esses comandos. Por exemplo, `playback` é documentado da seguinte forma:

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

o que significa que esse comando é usado da seguinte maneira:

* `playback` (sintaxe curta)
* `VideoPlayer.playback` (qualificado com o nome da classe do componente)
* `cont_videoPlayer.playback` (qualificado com a ID do componente, supondo que `cont` seja a ID do elemento do container)

Consulte Referência de [comando comum para todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Consulte Referência de [comando comum para todos os visualizadores - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
