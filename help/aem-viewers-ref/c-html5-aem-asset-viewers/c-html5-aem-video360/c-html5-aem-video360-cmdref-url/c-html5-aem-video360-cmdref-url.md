---
title: Referência de comando - URL
description: Documentação de referência de comando para o Video360 Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: eb7026cf-f28b-4426-ba64-b3472946d5d4
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# Referência de comando - URL{#command-reference-url}

Documentação de referência de comando para o Video360 Viewer.

Você pode definir qualquer comando de configuração no URL. Ou você pode usar os métodos de API `setParam()`, `setParams()` ou ambos para definir qualquer comando de configuração. Você também pode especificar qualquer atributo de configuração no registro de configuração do lado do servidor.

Você pode adicionar prefixos a alguns comandos de configuração com o nome da classe ou o nome da instância do componente SDK do Visualizador do HTML5 correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do contêiner de visualizador passado para o método de API `setContainerId()`. A documentação inclui prefixos opcionais para esses comandos. Por exemplo, `playback` é documentado da seguinte maneira:

```
[Video360Player.|<containerId>_video360Player].playback
```

Isso significa que esse comando é usado da seguinte maneira:

* `playback` (sintaxe curta)
* `Video360Player.playback` (qualificado com nome de classe de componente)
* `cont_video360Player.playback` (qualificado com ID de componente, supondo que `cont` seja a ID do elemento de contêiner)

Consulte [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Referência de comando comum a todos os visualizadores - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
