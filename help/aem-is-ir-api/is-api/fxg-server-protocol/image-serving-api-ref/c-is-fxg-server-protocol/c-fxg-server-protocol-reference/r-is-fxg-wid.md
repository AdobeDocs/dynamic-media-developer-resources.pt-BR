---
title: wid
description: Largura da exibição. Especifica a largura da imagem de resposta (exibir imagem).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# wid{#wid}

Largura da exibição. Especifica a largura da imagem de resposta (exibir imagem).

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Largura da imagem em pixels (int maior que 0), </p></td> 
 </tr> 
</table>

## Padrão {#section-830bae0b6bac440098444d7cdcb23e2e}

Se nenhuma delas `wid=`, `hei=`, nem `scale=` forem especificados, a imagem de resposta será o tamanho de exibição padrão especificado no arquivo FXG.

Os formatos de rasterização são renderizados usando o Tamanho de Visualização Padrão (ou a configuração DefaultPix). Clique em **[!UICONTROL Application Setup]** > **[!UICONTROL Publish Setup]** > **[!UICONTROL Image Server]**, em seguida, insira os valores de Largura e Altura. Tamanhos menores fornecem melhor desempenho. Salve as configurações e execute uma publicação do Servidor de imagens para aplicar uma alteração.

Se você aplicar uma `scale=1` , uma solicitação de formato rasterizado é processada no tamanho especificado no FXG.

## Exemplo {#section-2f72cb2653d54c6aaacf0d97521fb72c}

`http://server/is/agm/myRootId/myImageId?wid=200`

A menos que um formato seja especificado, a imagem é renderizada como um arquivo SWF. Nesse caso, altura e largura não têm significado, pois o SWF geralmente se expande para o tamanho da janela do navegador. Como resultado, `hei` e `wid` aplica-se somente aos formatos raster ou PDF. Os formatos de rasterização incluem:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha
