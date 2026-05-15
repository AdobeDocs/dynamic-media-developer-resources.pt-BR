---
title: quantizar
description: Quantização de cores. Especifica atributos de quantização de cores para a conversão de saída do GIF.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67247016-a038-4ed4-90ed-751eaf9c4881
TQID: 'https://experienceleague.adobe.com/m5e14tLMY1JAdZTzlw7iUZzXzL9yylP66MYi5XAeYtg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 189
ht-degree: 0%

---

# quantizar{#quantize}

Quantização de cores. Especifica atributos de quantização de cores para a conversão de saída do GIF.

` quantize= *`tipo`*[, *`pontilhamento`*[, *`númCores`*[, *`colorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> tipo </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {adaptive|web|mac} </span> tipo de paleta </p> <p>Selecione ' <span class="codeph"> web </span>' ou ' <span class="codeph"> mac </span>' para escolher uma paleta predefinida, ou defina como ' <span class="codeph"> adaptive </span>' para calcular uma paleta ideal para a imagem. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> pontilhamento </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off} </span> opções de pontilhamento </p> <p>Selecione "difuso" para difusão de erro Floyd- Steinberg ou "desligado" para desativar o pontilhamento. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> </p> </td> 
  <td class="stentry"> <p>Número de cores de saída (número inteiro) incluído na paleta ' <span class="codeph"> adaptativa </span>'. </p> <p> <span class="codeph"> <span class="varname"> numColors </span> </span> deve ser de 2 a 256. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList </span> </span> </p> </td> 
  <td class="stentry"> <p>Lista separada por vírgulas de cores forçadas do RGB no formato hex6. Permite que você especifique cores forçadas a serem incluídas em uma paleta ' <span class="codeph"> adaptável </span>'. Se o número de cores especificado for menor que <span class="codeph"> numColors </span>, as cores adicionais serão calculadas com base no conteúdo da imagem. </p> <p>Usado apenas se <span class="codeph"> fmt=gif </span> ou <span class="codeph"> fmt=gif-alpha </span>. Ignorado de outra forma. As cores especificadas com <span class="codeph"> <span class="varname"> colorList </span> </span> devem ser valores RGB no formato hex6 (consulte <span class="codeph"> color </span>); nenhum outro especificador de cor é permitido. </p> </td> 
 </tr> 
</table>

## Padrão {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Exemplo {#section-b3a979dc9ae3459baa093bf17310988f}

Gere uma miniatura GIF usando a paleta &#39; `web`&#39; e sem pontilhamento:

[!DNL `http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off`]

Converta a imagem em um GIF bi-tonal com transparência de cor-chave e force as cores para preto-e-branco:

[!DNL `http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`]
