---
description: InfoPanelPopup.infoServerUrl
solution: Experience Manager
title: InfoPanelPopup.infoServerUrl
uuid: 0d0f2fd8-b3fc-46fd-8720-9c4c51db9646
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%

---


# InfoPanelPopup.infoServerUrl{#infopanelpopup-infoserverurl}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]infoServerUrl= *`infoserverurl`*`

<table id="table_9A6258D9B0DA4A29AA8A6C9BBCFE3662"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> infoserverurl</span></span> </p> </td> 
   <td> <p>O modelo de URL do servidor de informações é usado para buscar pares de chave/valor para a substituição de variável no modelo de conteúdo do painel de informações. O modelo especificado normalmente contém espaços reservados para macro que são substituídos pelos dados reais antes que a solicitação seja enviada ao servidor. </p> <p><span class="codeph"> $1$</span> é substituído pelo valor de sobreposição que acionou  <span class="codeph"> </span> InfoPanelPopupacation. </p> <p><span class="codeph"> $2$</span> é substituído pelo número de sequência do quadro atual no conjunto de imagens. </p> <p><span class="codeph"> $3$</span> é substituído pelo primeiro elemento de caminho especificado no nome do conjunto pai do item atual. Normalmente corresponde à ID do catálogo. </p> <p><span class="codeph"> $4$</span> é substituído pelo seguinte elemento no caminho e corresponde à id do ativo. A sintaxe de solicitação do servidor de informações real depende do servidor de informações e é diferente de servidor para servidor. Por exemplo, o seguinte é um modelo típico de solicitação do servidor de informações do Dynamic Media: </p> <p><span class="codeph"> http://server_domain/s7info/s7/$3$/$4$/$1$</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Observe que, ao configurar o Pop-up do painel Informações, o código HTML e o código JavaScript passados para o Painel Informações são executados no computador do cliente. Portanto, verifique se esse código HTML e código JavaScript estão seguros.

## Propriedades {#section-71356e3c13244e62b0582980d9d05328}

Opcional.

## Padrão {#section-22e9af803f724434807d34e200eb7518}

Nenhum.

## Exemplo {#section-4f70fa4705c54452893c72c9da7e998a}

`infoServerUrl= http://s7info1.scene7.com/s7info/s7/$3$/$4$/$1$`
