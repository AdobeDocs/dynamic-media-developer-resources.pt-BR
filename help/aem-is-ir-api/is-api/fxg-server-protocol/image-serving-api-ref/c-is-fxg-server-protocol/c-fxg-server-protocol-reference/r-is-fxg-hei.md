---
description: Exibir altura. Especifica a altura da imagem de resposta.
solution: Experience Manager
title: hei
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---


# hei{#hei}

Exibir altura. Especifica a altura da imagem de resposta.

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Altura da imagem em pixels (int maior que 0). </p></td> 
 </tr> 
</table>

Os formatos raster são renderizados usando o Tamanho de exibição padrão (ou a configuração DefaultPix ). Clique em **[!UICONTROL Application Setup]** > **[!UICONTROL Publish Setup]** > **[!UICONTROL Image Server]** e insira os valores de Largura e Altura. Tamanhos menores proporcionam melhor desempenho. Você deve salvar suas configurações e executar uma Publicação de disponibilização de imagens para aplicar uma alteração.

Se você aplicar um comando `scale=1`, uma solicitação de formato raster será renderizada no tamanho especificado no FXG.

## Padrão {#section-76ee3daa77cb468ab310821357cc9404}

Se `wid=`, `hei=` ou `scale=` não forem especificadas, a imagem de resposta será o tamanho de exibição padrão especificado no arquivo FXG.

## Exemplo {#section-a91c14d31e71481ba054412d9f642885}

[!DNL http://server/is/agm/myRootId/myImageId?hei=200]

A menos que um formato seja especificado, a imagem é renderizada como um arquivo SWF. Nesse caso, altura e largura não têm significado, porque o SWF geralmente se expande para o tamanho da janela do navegador. Como resultado, hei e wid se aplicam apenas aos formatos raster ou PDF. Os formatos de raster incluem:

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alfa
* TIF-alfa
* PNG-alfa

