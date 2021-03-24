---
description: Documentação de referência de comando do visualizador do Video360.
solution: Experience Manager
title: Referência de comando - URL
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo 360 VR
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Referência de comando - URL{#command-reference-url}

Documentação de referência de comando do visualizador do Video360.

Você pode definir qualquer comando de configuração no URL. Ou você pode usar os métodos da API `setParam()`, ou `setParams()`, ou ambos para definir qualquer comando de configuração. Você também pode especificar qualquer atributo de configuração no registro de configuração do lado do servidor.

Você pode prefixar alguns comandos de configuração com o nome da classe ou o nome da instância do componente SDK do Visualizador de HTML5 correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do contêiner do visualizador passado para o método de API `setContainerId()` . A documentação inclui prefixos opcionais para esses comandos. Por exemplo, `playback` está documentado da seguinte maneira:

```
[Video360Player.|<containerId>_video360Player].playback
```

o que significa que esse comando é usado da seguinte maneira:

* `playback` (sintaxe curta)
* `Video360Player.playback` (qualificado com o nome da classe do componente)
* `cont_video360Player.playback` (qualificado com a ID do componente, supondo que  `cont` seja a ID do elemento do contêiner)

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum a todos os visualizadores - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
