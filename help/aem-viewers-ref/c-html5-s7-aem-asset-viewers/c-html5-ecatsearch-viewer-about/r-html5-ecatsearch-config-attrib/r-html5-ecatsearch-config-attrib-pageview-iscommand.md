---
description: PageView.iscommand
solution: Experience Manager
title: PageView.iscommand
topic: Dynamic Media
uuid: 32bfd041-e44c-4a78-a923-896a85d8f75f
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 1%

---


# PageView.iscommand{#pageview-iscommand}

[!DNL `[PageView.|<containerId>_pageView.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> A string de comando do Servidor de imagens que é aplicada à imagem da página. Se especificado no URL, todas as ocorrências de <span class="codeph"> &amp;</span> e <span class="codeph"> =</span> devem ser codificadas por HTTP como <span class="codeph"> %26</span> e <span class="codeph"> %3D</span>, respectivamente. </p> <p> <p>Observação:  Comandos de manipulação de dimensionamento de imagem não são suportados. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-df5a0604766b4ac2b9a6742b377e427c}

Opcional.

## Padrão {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

Nenhum.

## Exemplo {#section-813de2905d6c44c0991cfe0931581462}

Quando especificado no URL do visualizador.

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

Quando especificado nos dados de configuração.

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
