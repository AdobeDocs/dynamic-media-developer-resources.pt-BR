---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: f4bb0087-1e49-47e2-84b4-44b92fade36a
TQID: 'https://experienceleague.adobe.com/en4zktUgJGVG-e0fahRGTxasP3CVxhgfie6d0e3q6r4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 198
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
