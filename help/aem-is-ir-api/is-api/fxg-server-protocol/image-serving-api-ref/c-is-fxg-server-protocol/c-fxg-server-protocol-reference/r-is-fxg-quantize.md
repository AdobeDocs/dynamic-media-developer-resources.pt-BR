---
description: Quantificação de cores. Especifica atributos de quantificação de cores para conversão de saída GIF.
seo-description: Quantificação de cores. Especifica atributos de quantificação de cores para conversão de saída GIF.
seo-title: quantificar
solution: Experience Manager
title: quantificar
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 624cdc45-51f2-4b18-a658-311770974521
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---


# quantize{#quantize}

Quantificação de cores. Especifica atributos de quantificação de cores para conversão de saída GIF.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> Tipo de  </span> paleta {adaptive|web|mac} </p> <p>Selecione ' <span class="codeph"> web </span>' ou ' <span class="codeph"> mac </span>' para escolher uma paleta predefinida, ou defina como ' <span class="codeph"> adaptativa </span>' para calcular uma paleta ideal para a imagem. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> pontilhado  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off} opções de  </span> pontilhamento </p> <p>Selecione "difuso" para difusão de erros Floyd-Steinberg ou "desligado" para desativar o pontilhamento. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
  <td class="stentry"> <p>Número de cores de saída (número inteiro) incluídas na paleta ' <span class="codeph"> adaptativa </span>'. </p> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> deve estar entre 2 e 256. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
  <td class="stentry"> <p>Lista separada por vírgulas de cores RGB forçadas no formato hex6. Permite que você especifique cores forçadas a serem incluídas em uma paleta ' <span class="codeph"> adaptativa </span>'. Se o número de cores especificado for menor que <span class="codeph"> numColors </span>, as cores adicionais serão calculadas com base no conteúdo da imagem. </p> <p>Usado somente se <span class="codeph"> fmt=gif </span> ou <span class="codeph"> fmt=gif-alfa </span>. Caso contrário, ignorado. As cores especificadas com <span class="codeph"> <span class="varname"> colorList </span> </span> devem ser valores RGB no formato hex6 (consulte <span class="codeph"> color </span>); não são permitidos outros especificadores de cor. </p> </td> 
 </tr> 
</table>

## Padrão {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Exemplo {#section-b3a979dc9ae3459baa093bf17310988f}

Gere uma miniatura GIF usando a paleta &#39; `web`&#39; e sem pontilhamento:

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

Converta a imagem em um GIF bi-tonal com transparência de cores chave e força as cores a preto e branco:

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
