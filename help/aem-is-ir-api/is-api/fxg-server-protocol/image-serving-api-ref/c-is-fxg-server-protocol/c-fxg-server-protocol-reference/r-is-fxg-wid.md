---
description: Largura da exibição. Especifica a largura da imagem da resposta (imagem de exibição).
seo-description: Largura da exibição. Especifica a largura da imagem da resposta (imagem de exibição).
seo-title: wid
solution: Experience Manager
title: wid
uuid: b59b936c-abab-4f9d-95ca-0a09743ba0fb
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---


# wid{#wid}

Largura da exibição. Especifica a largura da imagem da resposta (imagem de exibição).

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Largura da imagem em pixels (int maior que 0), </p></td> 
 </tr> 
</table>

## Padrão {#section-830bae0b6bac440098444d7cdcb23e2e}

Se `wid=`, `hei=` ou `scale=` não forem especificadas, a imagem de resposta será o tamanho de exibição padrão especificado no arquivo FXG.

Os formatos raster são renderizados usando o Tamanho de exibição padrão (ou a configuração DefaultPix ). Clique em **[!UICONTROL Application Setup]** > **[!UICONTROL Publish Setup]** > **[!UICONTROL Image Server]** e insira os valores de Largura e Altura. Tamanhos menores proporcionam melhor desempenho. Você deve salvar suas configurações e executar uma Publicação de disponibilização de imagens para aplicar uma alteração.

Se você aplicar um comando `scale=1`, uma solicitação de formato raster será renderizada no tamanho especificado no FXG.

## Exemplo {#section-2f72cb2653d54c6aaacf0d97521fb72c}

[!DNL http://server/is/agm/myRootId/myImageId?wid=200]

A menos que um formato seja especificado, a imagem é renderizada como um arquivo SWF. Nesse caso, altura e largura não têm significado, porque o SWF geralmente se expande para o tamanho da janela do navegador. Como resultado, hei e wid se aplicam apenas aos formatos raster ou PDF. Os formatos de raster incluem:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alfa
* TIF-alfa
* PNG-alfa

