---
title: Referência de comando - Atributos de configuração
description: Documentação de atributos de configuração para o Visualizador de vídeo de recorte inteligente.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
mini-toc-levels: 3
exl-id: 698c03b1-bec0-44bf-9c79-c66e0192344a
TQID: 'https://experienceleague.adobe.com/fTLIy9C3f-00e-wpBTVbQroziLWBo2YT8ieDrdlrnak'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 164
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
