---
description: Atributo de configuração para o visualizador do Video360.
seo-description: Atributo de configuração para o visualizador do Video360.
seo-title: Video360Player.ssl
solution: Experience Manager
title: Video360Player.ssl
uuid: 00c8295c-cc41-489c-a444-ba9189426a20
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo 360 VR
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 3%

---


# Video360Player.ssl{#video-player-ssl}

Atributo de configuração para o visualizador do Video360.

>[!NOTE]
>
>Esse atributo de configuração se aplica somente ao AEM 6.2 com instalação do [Feature Pack NPR-13480](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq620/featurepack/cq-6.2.0-featurepack-13480) e ao AEM 6.1 com instalação do [Feature Pack NPR-15011](https://www.adobeaemcloud.com/content/marketplace/marketplaceProxy.html?packagePath=/content/companies/public/adobe/packages/cq610/featurepack/cq-6.1.0-featurepack-15011).

`[Video360Player.|<containerId>_video360Player.]ssl=auto|on`

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

Consulte também [Entrega de vídeo seguro](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-securevideodelivery.md#concept-13f66fdd4a52494aa516cd0f36fdac27).
