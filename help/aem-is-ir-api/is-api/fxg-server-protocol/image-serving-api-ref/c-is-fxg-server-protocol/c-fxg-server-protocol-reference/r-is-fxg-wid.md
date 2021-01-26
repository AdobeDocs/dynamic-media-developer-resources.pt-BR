---
description: Largura da visualização. Especifica a largura da imagem de resposta (imagem de visualização).
seo-description: Largura da visualização. Especifica a largura da imagem de resposta (imagem de visualização).
seo-title: inteligência
solution: Experience Manager
title: inteligência
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b59b936c-abab-4f9d-95ca-0a09743ba0fb
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 0%

---


# wid{#wid}

Largura da visualização. Especifica a largura da imagem de resposta (imagem de visualização).

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Largura da imagem em pixels (int maior que 0), </p></td> 
 </tr> 
</table>

## Padrão {#section-830bae0b6bac440098444d7cdcb23e2e}

Se `wid=`, `hei=` ou `scale=` não forem especificados, a imagem de resposta será o tamanho de visualização padrão especificado no arquivo FXG.

Os formatos Rasterização são renderizados usando o Tamanho de Visualização padrão (ou a configuração DefaultPix). Clique em **[!UICONTROL Application Setup]** > **[!UICONTROL Publish Setup]** > **[!UICONTROL Image Server]** e insira os valores de Largura e Altura. Tamanhos menores proporcionam melhor desempenho. É necessário salvar suas configurações e executar um Publicação de disponibilização de imagem para aplicar uma alteração.

Se você aplicar um comando `scale=1`, uma solicitação de formato rasterizado será renderizada no tamanho especificado no FXG.

## Exemplo {#section-2f72cb2653d54c6aaacf0d97521fb72c}

[!DNL http://server/is/agm/myRootId/myImageId?wid=200]

A menos que um formato seja especificado, a imagem é renderizada como um arquivo SWF. Nesse caso, a altura e a largura não têm significado, pois o SWF geralmente se expande para o tamanho da janela do navegador. Como resultado, hei e wid só se aplicam aos formatos raster ou PDF. Os formatos de rasterização incluem:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alfa
* TIF-alfa
* PNG-alfa

