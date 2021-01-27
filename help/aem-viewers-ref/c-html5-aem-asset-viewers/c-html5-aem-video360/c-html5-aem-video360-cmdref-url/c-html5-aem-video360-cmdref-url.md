---
description: Documentação de referência de comando para o visualizador do Video360.
seo-description: Documentação de referência de comando para o visualizador do Video360.
seo-title: Referência de comando - URL
solution: Experience Manager
title: Referência de comando - URL
topic: Dynamic Media
uuid: 70c212d7-35ee-408f-abe4-19ba1e4d773d
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---


# Referência de comando - URL{#command-reference-url}

Documentação de referência de comando para o visualizador do Video360.

É possível definir qualquer comando de configuração no URL. Ou você pode usar os métodos de API `setParam()`, `setParams()` ou ambos para definir qualquer comando de configuração. Você também pode especificar qualquer atributo de configuração no registro de configuração do lado do servidor.

Você pode prefixar alguns comandos de configuração com o nome da classe ou da instância do componente SDK do Visualizador HTML5 correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do container do visualizador passado para o método da API `setContainerId()`. A documentação inclui prefixos opcionais para esses comandos. Por exemplo, `playback` está documentado da seguinte forma:

```
[Video360Player.|<containerId>_video360Player].playback
```

o que significa que esse comando é usado da seguinte maneira:

* `playback` (sintaxe curta)
* `Video360Player.playback` (qualificado com o nome da classe do componente)
* `cont_video360Player.playback` (qualificado com a ID do componente, supondo que essa  `cont` seja a ID do elemento do container)

Consulte [Referência de comando comum para todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum para todos os visualizadores - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
