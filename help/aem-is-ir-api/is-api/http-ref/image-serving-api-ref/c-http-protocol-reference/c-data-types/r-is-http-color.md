---
description: Valores de cor. Você pode especificar valores de cor usando notação hexadecimal, uma lista separada por vírgulas de valores de componentes ou decimais.
seo-description: Valores de cor. Você pode especificar valores de cor usando notação hexadecimal, uma lista separada por vírgulas de valores de componentes ou decimais.
seo-title: color
solution: Experience Manager
title: color
uuid: 61308b8e-eaac-4b2e-8500-2f9efa8a6ce8
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 11%

---


# color{#color}

Valores de cor. Você pode especificar valores de cor usando notação hexadecimal, uma lista separada por vírgulas de valores de componentes ou decimais.

<table id="simpletable_9EBE66066E854ABE978F8F7ADC66BDE3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> color</span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph">{{<span class="varname"> cinza</span>[, <span class="varname"> alfa</span>][g]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> vermelho</span>, <span class="varname"> verde</span>, <span class="varname"> azul</span>[ ,<span class="varname"> rgbAlpha</span>][r]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> ciano</span>,  <span class="varname"> magenta</span>,  <span class="varname"> amarelo</span>,  <span class="varname"> preto</span>[,alfa]k}|</span> </p> <p> <span class="codeph"> {0x{hex2|hex4}[g]}|</span> </p> <p> <span class="codeph">{[0x]{<span class="varname"> hex6</span> | <span class="varname"> hex8</span>}[r]}|</span> </p> <p> <span class="codeph"> {[0x]{<span class="varname"> hex8</span>|<span class="varname"> hex10</span>}k}[s]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> vermelho</span>,  <span class="varname"> verde</span>,  <span class="varname"> azul</span>,  <span class="varname"> rgbAlpha</span></span> </p> </td> 
  <td class="stentry"> <p>valor do componente de cor (0...255, decimal int) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> ciano</span>,  <span class="varname"> magenta</span>,  <span class="varname"> amarelo</span>,  <span class="varname"> preto</span>,  <span class="varname"> alfa</span></span> </p></td> 
  <td class="stentry"> <p>Valor do componente de cor CMYK (0,100 %, decimal int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cinza</span>,  <span class="varname"> alfa</span></span> </p> </td> 
  <td class="stentry"> <p>valor do componente de cor cinza (0...100%, decimal int) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex2</span> </span> </p></td> 
  <td class="stentry"> <p>valor de cor cinza hexadecimal de dois dígitos embalado (GG) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex4</span> </span> </p> </td> 
  <td class="stentry"> <p>cinza hexadecimal de quatro dígitos embalado com valor de cor alfa (GGAA) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex6</span> </span> </p> </td> 
  <td class="stentry"> <p>valor de cor RGB hexadecimal de seis dígitos compactado (RRGGBB) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex8</span> </span> </p> </td> 
  <td class="stentry"> <p>valor de cor RGBA hexadecimal de oito dígitos (RRGGBBAA) ou CMYK (CCMMMYKK) compactado (se especificado com o sufixo 'k') </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex10</span> </span> </p></td> 
  <td class="stentry"> <p>CMYK hexadecimal de dez dígitos compactado com valor alfa (CCYMMKKAA) </p> </td> 
 </tr> 
</table>

Os valores dos componentes decimais para cores RGB estão no intervalo 0...255. Os valores dos componentes decimais para CMYK e cinza estão no intervalo 0,100%. Todos os valores de componentes hexadecimais estão no intervalo 0...0xFF.

Pressupõe-se que os valores dos componentes de cor sejam independentes do valor alfa (não pré-multiplicado).

Todos os valores de cor, prefixos e sufixos não diferenciam maiúsculas de minúsculas.

O sufixo de tipo &#39;k&#39; é necessário para valores de cores CMYK. Um sufixo de tipo pode ser especificado opcionalmente para valores de cores RGB e cinza.

O prefixo &#39;0x&#39; é necessário para valores de cores cinza hexadecimais.

O sufixo &#39;s&#39; especifica que o valor da cor está associado ao espaço de cores de entrada (fonte) correspondente ao tipo de pixel do valor da cor (definido com `attribute::IccProfileSrc*`). Se esse sufixo não estiver presente, o valor da cor será associado ao espaço de cores de saída (destino) (definido com `icc=` ou `attribute::IccProfile*`).

## Padrão {#section-737082a7da544acca8092a48d88480e7}

Se um valor alfa não for especificado explicitamente, é considerado 255, 0xFF ou 100% (totalmente opaco).

## Exemplos {#section-4ac69026349949f8b595a6d4a9ce474d}

Alguns exemplos de especificadores de cores válidos e seu tipo de pixel, valor de cor, valor alfa e espaço de cores padrão correspondentes:

<table id="table_1539E74A1EC545F1B5398D86A27079D1"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>color</i> </b> </th> 
   <th class="entry"> <b>Tipo de pixel</b> </th> 
   <th class="entry"> <b>Valor da cor</b> </th> 
   <th class="entry"> <b>Valor alfa</b> </th> 
   <th class="entry"> <b>Espaço de cores padrão  </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>0.100.200 </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>0.100.200 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0.100.200.200rs </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>0.100.200 </p> </td> 
   <td> <p>200 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x010203S </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>1,2,3 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>a0b1c2d3R </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>160 177 194 </p> </td> 
   <td> <p>211º </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>100S </p> </td> 
   <td> <p>cinza </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>50,75 g </p> </td> 
   <td> <p>cinza </p> </td> 
   <td> <p>50% </p> </td> 
   <td> <p>75% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0X70G </p> </td> 
   <td> <p>cinza </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0xddeegs </p> </td> 
   <td> <p>cinza </p> </td> 
   <td> <p>87% </p> </td> 
   <td> <p>93% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>94,11,50,33 k </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>94-11-50-33% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>22,23,24,25,26KS </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>22-23-24-25% </p> </td> 
   <td> <p>26% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>38393A3bK </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>56-57-58-59% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x0a0b0C0d0eks </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>10-11-12-13% </p> </td> 
   <td> <p>14% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

O espaço de cores de saída especificado com `icc=` aplica-se em vez do espaço de cores padrão quando o tipo de pixel de uma cor de saída corresponde ao tipo de pixel da imagem de saída.
