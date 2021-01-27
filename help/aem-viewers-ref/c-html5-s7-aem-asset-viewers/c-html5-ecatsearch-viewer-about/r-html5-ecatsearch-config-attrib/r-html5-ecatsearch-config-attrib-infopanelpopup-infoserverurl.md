---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
topic: Dynamic Media
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---


# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

[!DNL `[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`]

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>O modelo de URL do servidor de informações é usado para buscar pares de chaves/valores para a substituição de variáveis no modelo de conteúdo do painel de informações. O modelo especificado normalmente contém espaços reservados para macro que são substituídos pelos dados reais antes de a solicitação ser enviada ao servidor. </p> <p><span class="codeph"> $1$</span> é substituído pelo valor de sobreposição que disparou a  <span class="codeph"> </span> InfoPanelPopupactivation. </p> <p><span class="codeph"> $2$</span> é substituído pelo número de sequência do quadro atual no conjunto de imagens. </p> <p><span class="codeph"> $3$</span> é substituído pelo primeiro elemento de caminho especificado no nome do conjunto pai do item atual. Normalmente, corresponde à ID do catálogo. </p> <p><span class="codeph"> $4$</span> é substituído pelo seguinte elemento no caminho e corresponde à ID do ativo. A sintaxe real de solicitação do servidor de informações depende do servidor de informações e é diferente de servidor para servidor. Por exemplo, este é um modelo de solicitação típico do servidor de informações da Dynamic Media: </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ao configurar o Pop-up do painel Informações, o código HTML e o código JavaScript passados para o Painel Informações são executados no computador do cliente. Portanto, verifique se o código HTML e o código JavaScript estão protegidos.

## Propriedades {#section-71356e3c13244e62b0582980d9d05328}

Opcional.

## Padrão {#section-22e9af803f724434807d34e200eb7518}

Nenhum.

## Exemplo {#section-4f70fa4705c54452893c72c9da7e998a}

[!DNL `infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`]
