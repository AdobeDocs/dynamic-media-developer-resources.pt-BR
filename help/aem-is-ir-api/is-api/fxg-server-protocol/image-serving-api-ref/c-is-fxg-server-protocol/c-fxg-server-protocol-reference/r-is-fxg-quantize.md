---
description: Quantificação de cores. Especifica atributos de quantificação de cores para conversão de saída GIF.
solution: Experience Manager
title: quantizar
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---


# quantizar{#quantize}

Quantificação de cores. Especifica atributos de quantificação de cores para conversão de saída GIF.

` quantize= *``*[, *``*[, *``*[, *`typedithernumColorscolorList`*]]]`

<table id="simpletable_6BF155FCB8224E7EBFC8D8375AD26A71"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> type  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> Tipo de  </span> paleta {adaptive|web|mac} </p> <p>Selecione ' <span class="codeph"> web </span>' ou ' <span class="codeph"> mac </span>' para escolher uma paleta predefinida ou defina como ' <span class="codeph"> adaptável </span>' para calcular uma paleta ideal para a imagem. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> tonalidade  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> {diffuse|off} opções  </span> de pontilhamento </p> <p>Selecione "difuso" para a difusão de erros Floyd-Steinberg ou "desativado" para desativar a ligação à ranhura. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> </p> </td> 
  <td class="stentry"> <p>Número de cores de saída (número inteiro) incluídas na paleta ' <span class="codeph"> adaptável </span>'. </p> <p> <span class="codeph"> <span class="varname"> numColors  </span> </span> deve estar entre 2 e 256. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colorList  </span> </span> </p> </td> 
  <td class="stentry"> <p>Lista separada por vírgulas de cores RGB forçadas no formato hex6. Permite que você especifique cores forçadas a serem incluídas em uma paleta ' <span class="codeph"> adaptável </span>'. Se o número de cores especificado for menor que <span class="codeph"> numColors </span>, cores adicionais serão calculadas com base no conteúdo da imagem. </p> <p>Usado somente se <span class="codeph"> fmt=gif </span> ou <span class="codeph"> fmt=gif-alpha </span>. Caso contrário, ignorado. As cores especificadas com <span class="codeph"> <span class="varname"> colorList </span> </span> devem ser valores RGB no formato hexadecimal (consulte <span class="codeph"> cor </span>); não são permitidos outros especificadores de cores. </p> </td> 
 </tr> 
</table>

## Padrão {#section-dd2762cb19344e599f5283986973ba1b}

`quantize=adaptive,diffuse,256`

## Exemplo {#section-b3a979dc9ae3459baa093bf17310988f}

Gere uma miniatura GIF usando a paleta &#39; `web`&#39; e sem pontilhamento:

[!DNL http://server/myRootId/myImageId?req=tmb&fmt=gif&quantize=web,off]

Converta a imagem em um GIF bi-tonal com transparência de cores chave e force as cores para preto e branco:

[!DNL http://server/is/agm/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff]
