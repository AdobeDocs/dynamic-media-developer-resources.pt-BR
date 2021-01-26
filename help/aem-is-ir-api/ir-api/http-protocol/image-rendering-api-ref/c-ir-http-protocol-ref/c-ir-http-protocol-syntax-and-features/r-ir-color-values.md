---
description: Os valores de cor para os atributos color= e bgc= podem ser especificados usando uma lista de valores de componentes decimais separados por vírgulas ou uma notação hexadecimal, similar ao HTML.
seo-description: Os valores de cor para os atributos color= e bgc= podem ser especificados usando uma lista de valores de componentes decimais separados por vírgulas ou uma notação hexadecimal, similar ao HTML.
seo-title: Valores de cor
solution: Experience Manager
title: Valores de cor
topic: Dynamic Media Image Serving - Image Rendering API
uuid: f8e3a8e7-3e0c-4ee6-8434-caba1f2bea1f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 7%

---


# Valores de cor{#color-values}

Os valores de cor para os atributos color= e bgc= podem ser especificados usando uma lista de valores de componentes decimais separados por vírgulas ou uma notação hexadecimal, similar ao HTML.

<table id="simpletable_9B3A231D5BB14A3DB2B42B341E198341"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cor</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">{vermelho, verde, azul} | cinza } | { [ 0x ] hex6 } | { 0xhex2 }</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>vermelho, verde, azul, cinza</i> </p></td> 
  <td class="stentry"> <p>Valor do componente colorido (0...255, número inteiro decimal). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>hex6</i> </p></td> 
  <td class="stentry"> <p>Valor de cor RGB hexadecimal de seis dígitos (RRGGBB) compactado. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>hex2</i> </p></td> 
  <td class="stentry"> <p>Valor de cor cinza hexadecimal de dois dígitos compactado (0...FF). </p></td> 
 </tr> 
</table>

## Exemplos {#section-a78732151d584e84abeb99f9ce8d7c24}

Alguns exemplos de especificadores de cores válidos e sua interpretação de valor de cor RGB correspondente:

<table id="simpletable_837B3173020240A5B7B2DB2F4CC57352"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0.100.200 </p></td> 
  <td class="stentry"> <p>(0.100.200) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>128 </p></td> 
  <td class="stentry"> <p>(128 128 128) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0x010203 </p></td> 
  <td class="stentry"> <p>(1,2,3) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>00b1c2 </p></td> 
  <td class="stentry"> <p>(160 177 194) </p></td> 
 </tr> 
</table>

## Consulte também {#section-207d5cb918a94736a27445faa58917d3}

[color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa),  [bgc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-bgc.md#reference-3f5c78cea01c4a85aa582076d23aebb0),  [grout=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
