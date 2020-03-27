---
description: Largura da Visualização. Especifica a largura da imagem de resposta (imagem de visualização).
seo-description: Largura da Visualização. Especifica a largura da imagem de resposta (imagem de visualização).
seo-title: inteligência
solution: Experience Manager
title: inteligência
topic: Scene7 Image Serving - Image Rendering API
uuid: b59b936c-abab-4f9d-95ca-0a09743ba0fb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# inteligência{#wid}

Largura da Visualização. Especifica a largura da imagem de resposta (imagem de visualização).

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Largura da imagem em pixels (int maior que 0), </p></td> 
 </tr> 
</table>

## Padrão {#section-830bae0b6bac440098444d7cdcb23e2e}

Se nem `wid=`, `hei=`nem `scale=` forem especificados, a imagem de resposta será o tamanho de visualização padrão especificado no arquivo FXG.

Os formatos Rasterização são renderizados usando o Tamanho de Visualização padrão (ou a configuração DefaultPix). Clique em Configuração **[!UICONTROL do]** aplicativo > **[!UICONTROL Publicar configuração]** > Servidor **[!UICONTROL de]** imagem e insira os valores de Largura e Altura. Tamanhos menores proporcionam melhor desempenho. É necessário salvar suas configurações e executar um Publicação de disponibilização de imagem para aplicar uma alteração.

Se você aplicar um `scale=1` comando, uma solicitação de formato rasterizado será renderizada no tamanho especificado no FXG.

## Example {#section-2f72cb2653d54c6aaacf0d97521fb72c}

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

