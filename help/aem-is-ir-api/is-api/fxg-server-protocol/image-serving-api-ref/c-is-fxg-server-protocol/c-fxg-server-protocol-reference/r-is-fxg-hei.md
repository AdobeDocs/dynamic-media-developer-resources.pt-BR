---
description: Altura da Visualização. Especifica a altura da imagem de resposta.
seo-description: Altura da Visualização. Especifica a altura da imagem de resposta.
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 6f7e580b-6399-4661-b5d9-8044574ba124
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# hei{#hei}

Altura da Visualização. Especifica a altura da imagem de resposta.

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Altura da imagem em pixels (int maior que 0). </p></td> 
 </tr> 
</table>

Os formatos Rasterização são renderizados usando o Tamanho de Visualização padrão (ou a configuração DefaultPix). Clique em Configuração **[!UICONTROL do]** aplicativo > **[!UICONTROL Publicar configuração]** > Servidor **[!UICONTROL de]** imagem e insira os valores de Largura e Altura. Tamanhos menores proporcionam melhor desempenho. É necessário salvar suas configurações e executar um Publicação de disponibilização de imagem para aplicar uma alteração.

Se você aplicar um `scale=1` comando, uma solicitação de formato rasterizado será renderizada no tamanho especificado no FXG.

## Padrão {#section-76ee3daa77cb468ab310821357cc9404}

Se nem `wid=`, `hei=`nem `scale=` forem especificados, a imagem de resposta será o tamanho de visualização padrão especificado no arquivo FXG.

## Example {#section-a91c14d31e71481ba054412d9f642885}

[!DNL http://server/is/agm/myRootId/myImageId?hei=200]

A menos que um formato seja especificado, a imagem é renderizada como um arquivo SWF. Nesse caso, a altura e a largura não têm significado, pois o SWF geralmente se expande para o tamanho da janela do navegador. Como resultado, hei e wid só se aplicam aos formatos raster ou PDF. Os formatos de rasterização incluem:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alfa
* TIF-alfa
* PNG-alfa

