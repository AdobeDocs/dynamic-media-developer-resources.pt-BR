---
title: hei
description: Altura da exibição. Especifica a altura da imagem de resposta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---

# hei{#hei}

Altura da exibição. Especifica a altura da imagem de resposta.

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Altura da imagem em pixels (int maior que 0). </p></td> 
 </tr> 
</table>

Os formatos de rasterização são renderizados usando o Tamanho de Visualização Padrão (ou a configuração DefaultPix). Selecione **[!UICONTROL Application Setup]** > **[!UICONTROL Publish Setup]** > **[!UICONTROL Image Server]** e insira seus valores de Largura e Altura. Tamanhos menores fornecem melhor desempenho. Salve as configurações e execute uma publicação do Servidor de imagens para aplicar uma alteração.

Se você aplicar um comando `scale=1`, uma solicitação de formato rasterizado será renderizada no tamanho especificado no FXG.

## Padrão {#section-76ee3daa77cb468ab310821357cc9404}

Se `wid=`, `hei=` ou `scale=` não forem especificados, a imagem de resposta será o tamanho de exibição padrão especificado no arquivo FXG.

## Exemplo {#section-a91c14d31e71481ba054412d9f642885}

[!DNL `http://server/is/agm/myRootId/myImageId?hei=200`]

A menos que um formato seja especificado, a imagem é renderizada como um arquivo SWF. Nesse caso, altura e largura não têm significado, pois o SWF geralmente se expande para o tamanho da janela do navegador. Como resultado, hei e wid só se aplicam aos formatos raster ou PDF. Os formatos de rasterização incluem:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha
