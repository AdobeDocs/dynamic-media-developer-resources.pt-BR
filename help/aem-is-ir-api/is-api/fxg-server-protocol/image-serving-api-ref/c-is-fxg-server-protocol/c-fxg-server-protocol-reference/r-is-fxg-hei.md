---
title: hei
description: Altura da exibição. Especifica a altura da imagem de resposta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
TQID: 'https://experienceleague.adobe.com/Tpl8zVXQVzs3isa26A3YvnOzs6gqpz3-4L-qDBx-eK0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 168
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
