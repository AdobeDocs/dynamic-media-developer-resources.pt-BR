---
description: Quantização de cores. Especifica atributos de quantização de cores para a conversão de saída de GIF.
solution: Experience Manager
title: quantizar
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 0%

---

# quantizar{#quantize}

Quantização de cores. Especifica atributos de quantização de cores para a conversão de saída de GIF.

` quantize= *`type`*[, *`pontilhamento`*[, *`numColors`*[, *`colorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac} </span> tipo de paleta </p> <p>Selecionar ' <span class="codeph"> web </span>' ou ' <span class="codeph"> mac </span>' para escolher uma paleta predefinida ou definir como ' <span class="codeph"> adaptável </span>' para calcular uma paleta ideal para a imagem. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> pontilhamento </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off} </span> opções de pontilhamento </p> <p>Selecione "difuso" para difusão de erro Floyd- Steinberg ou "desligado" para desativar o pontilhamento. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
  <td class="stentry"> <p>Número de cores de saída (número inteiro) incluídas no ' <span class="codeph"> adaptável </span>paleta '. </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> deve estar entre 2 e 256. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
  <td class="stentry"> <p>Lista separada por vírgulas de cores de RGB forçadas no formato hex6. Permite que você especifique cores forçadas para serem incluídas em um ' <span class="codeph"> adaptável </span>paleta '. Se o número de cores especificado for menor que <span class="codeph"> numColors </span>, as cores adicionais são calculadas com base no conteúdo da imagem. </p> <p>Usado somente se <span class="codeph"> fmt=gif </span> ou <span class="codeph"> fmt=gif-alpha </span>. Ignorado de outra forma. As cores especificadas com <span class="codeph"> <span class="varname"> colorList </span> </span> deve ser valores de RGB no formato hex6 (consulte <span class="codeph"> cor </span>); nenhum outro especificador de cor é permitido. </p> </td> 
 </tr> 
</table>

## Padrão {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Exemplo {#section-b3a979dc9ae3459baa093bf17310988f}

Gere uma miniatura de GIF usando o &#39; `web`&#39; paleta e sem pontilhamento:

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

Converta a imagem em um GIF bi-tonal com transparência de cor-chave e force as cores para preto e branco:

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
