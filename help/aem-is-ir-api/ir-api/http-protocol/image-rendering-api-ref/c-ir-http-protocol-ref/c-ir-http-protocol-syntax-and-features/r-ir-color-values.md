---
title: Valores de cor
description: Os valores de cor para os atributos color= e bgc= podem ser especificados usando uma lista de valores de componente decimais separados por vírgula ou uma notação hexadecimal, semelhante ao HTML.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 608ff0f1-4fbd-4e32-af07-3a62569d14c7
TQID: 'https://experienceleague.adobe.com/KZibvornkiv7U3dfqaJQncz-dBNtrF2a58oENB36ojg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 4%

---

# Valores de cor{#color-values}

Os valores de cor para os atributos `color=` e `bgc=` podem ser especificados usando uma lista de valores de componente decimais separados por vírgula ou uma notação hexadecimal, semelhante ao HTML.

<table id="simpletable_9B3A231D5BB14A3DB2B42B341E198341"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cor</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">{ {red , green , blue} | cinza } | { [ 0x ] hex6 } | { 0xhex2 }</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>vermelho, verde, azul, cinza</i> </p></td> 
  <td class="stentry"> <p>Valor do componente de cor (0 a 255, número inteiro decimal). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>hexa6</i> </p></td> 
  <td class="stentry"> <p>Valor de cor RGB hexadecimal de seis dígitos compactado (RRGGBB). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>hex2</i> </p></td> 
  <td class="stentry"> <p>Valor de cor cinza hexadecimal de dois dígitos compactado (0...FF). </p></td> 
 </tr> 
</table>

## Exemplos {#section-a78732151d584e84abeb99f9ce8d7c24}

Alguns exemplos de especificadores de cor válidos e sua interpretação de valor de cor RGB correspondente:

<table id="simpletable_837B3173020240A5B7B2DB2F4CC57352"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,100,200 </p></td> 
  <td class="stentry"> <p>(0,100,200) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>128 </p></td> 
  <td class="stentry"> <p>(128,128,128) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0x010203 </p></td> 
  <td class="stentry"> <p>(1,2,3) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>00b1c2 </p></td> 
  <td class="stentry"> <p>(160,177,194) </p></td> 
 </tr> 
</table>

## Consulte também {#section-207d5cb918a94736a27445faa58917d3}

[color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa), [bgc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-bgc.md#reference-3f5c78cea01c4a85aa582076d23aebb0), [grout=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)

