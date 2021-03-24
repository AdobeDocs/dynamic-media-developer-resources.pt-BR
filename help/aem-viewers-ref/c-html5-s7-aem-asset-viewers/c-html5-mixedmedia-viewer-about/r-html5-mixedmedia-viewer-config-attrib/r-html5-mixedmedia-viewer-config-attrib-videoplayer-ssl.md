---
description: Atributo de configuração para Visualizador de vídeo de mídia mista.
solution: Experience Manager
title: VideoPlayer.ssl
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---


# VideoPlayer.ssl{#videoplayer-ssl}

Atributo de configuração para Visualizador de vídeo de mídia mista.

>[!NOTE]
>
>Esse atributo de configuração se aplica somente ao AEM 6.2 com instalação do [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) e ao AEM 6.1 com instalação do [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

`[VideoPlayer.|<containerId>_videoPlayer.]ssl=auto|on`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|on</span> </p> </td> 
   <td colname="col2"> <p> Controla se o vídeo é entregue por uma conexão SSL segura (HTTPS) ou por uma conexão insegura (HTTP). </p> <p>Quando definido como <span class="codeph"> auto</span> o protocolo de entrega de vídeo é herdado do protocolo da página da Web de incorporação. Se a página da Web for carregada por HTTPS, o vídeo também será entregue por HTTPS, e vice-versa. Se a página da Web estiver em HTTP, o vídeo será entregue via HTTP. </p> <p>Quando definido como <span class="codeph"> em</span>, a entrega de vídeo sempre ocorre por uma conexão segura independentemente do protocolo da página da Web. </p> <p>Afeta apenas a entrega de vídeo publicado e é ignorado para visualização de vídeo no modo Autor. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
ssl=on
```

<!--<a id="section_5943AC73316749C68761FF7F74DA7547"></a>-->

Consulte também [Entrega de vídeo seguro](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-securevideodelivery.md#concept-4d155111df9f469aa6c6d7b41e959dcb).
