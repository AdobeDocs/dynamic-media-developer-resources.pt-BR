---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: f4bb0087-1e49-47e2-84b4-44b92fade36a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

[!DNL `[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`]

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>O modelo de URL do servidor de informações é usado para buscar pares de chave/valor para a substituição de variável no modelo de conteúdo do painel de informações. O modelo especificado geralmente contém marcadores de posição de macro que são substituídos pelos dados reais antes que a solicitação seja enviada ao servidor. </p> <p><span class="codeph"> $1$</span> é substituído pelo valor de substituição que disparou a ativação de <span class="codeph"> InfoPanelPopup</span>. </p> <p><span class="codeph"> $2$</span> é substituído pelo número de sequência do quadro atual no conjunto de imagens. </p> <p><span class="codeph"> $3$</span> é substituído pelo primeiro elemento de caminho especificado no nome do conjunto pai do item atual. Normalmente, corresponde à ID do catálogo. </p> <p><span class="codeph"> $4$</span> é substituído pelo seguinte elemento no caminho e corresponde à id do ativo. A sintaxe de solicitação do servidor de informações real depende do servidor de informações e é diferente de servidor para servidor. Por exemplo, este é um modelo típico de solicitação de servidor de informações do Dynamic Media: </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Observe que, ao configurar o Pop-up Painel de informações, o código do HTML e do JavaScript passados para o Painel de informações serão executados no computador do cliente. Portanto, verifique se esse código HTML e JavaScript são seguros.

## Propriedades {#section-71356e3c13244e62b0582980d9d05328}

Opcional.

## Padrão {#section-22e9af803f724434807d34e200eb7518}

Nenhum.

## Exemplo {#section-4f70fa4705c54452893c72c9da7e998a}

[!DNL `infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`]
