---
title: Referência de comando - Atributos de configuração
description: Documentação de atributos de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 80b7971c-82dc-47a2-adde-9e061a0f856d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Documentação de atributos de configuração para o Visualizador de vídeo interativo.

Qualquer comando de configuração pode ser definido na URL ou usando `setParam()`, `setParams()` ou ambos os métodos de API. Qualquer atributo de configuração também pode ser especificado no registro de configuração do lado do servidor.

Alguns comandos de configuração podem receber o nome da classe ou o nome da instância do componente SDK do visualizador correspondente. Um nome de instância do componente é dinâmico e depende da ID do elemento DOM do contêiner de visualizador passado para o método de API `setContainerId()`. A documentação inclui um prefixo opcional para esses comandos. Por exemplo, o comando `playback` está documentado da seguinte maneira:

`[VideoPlayer.|<containerId>_videoPlayer].playback`

And significa que você pode usar o seguinte comando como:

* `playback` (sintaxe curta)
* `VideoPlayer.playback` (qualificado com nome de classe de componente)
* `cont_videoPlayer.playback` (qualificado com ID de componente, supondo que `cont` seja a ID do elemento de contêiner)

Consulte também [Referência de comando comum a todos os visualizadores - Atributos de configuração](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
