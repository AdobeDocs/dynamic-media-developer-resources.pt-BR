---
description: Esses comandos são usados para selecionar grupos de vinhetas, objetos, subáreas de grupos ou objetos.
seo-description: Esses comandos são usados para selecionar grupos de vinhetas, objetos, subáreas de grupos ou objetos.
seo-title: Comandos de seleção
solution: Experience Manager
title: Comandos de seleção
topic: Dynamic Media Image Serving - Image Rendering API
uuid: fac4080b-3b7e-46ac-a564-3a7eff80c9eb
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# Comandos de seleção{#selection-commands}

Esses comandos são usados para selecionar grupos de vinhetas, objetos, subáreas de grupos ou objetos.

O comando ou o material, ou ambos, são especificados depois desse comando de seleção e antes do próximo comando de seleção (ou do final da solicitação) ser aplicado ao item selecionado. Os comandos de seleção delimitam segmentos de especificação de material (MSS).

<table id="simpletable_028957E516644FE8A7B1BC056A32FCD1"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a" type="reference" format="dita" scope="local"> obj</a> </span> </p></td> 
  <td class="stentry"> <p>Selecione um grupo de vinhetas ou objeto por nome. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b" type="reference" format="dita" scope="local"> sel</a></span> </p></td> 
  <td class="stentry"> <p>Selecione um grupo de vinheta ou objeto por localização de pixel. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-decal.md#reference-3a5f1adc7fe24c91aa5655d64038e857" type="reference" format="dita" scope="local"> decalque</a></span> </p></td> 
  <td class="stentry"> <p>Selecione a área de decalque do objeto selecionado. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sub.md#reference-3cedba817f3c401495ba32bd1bf9b383" type="reference" format="dita" scope="local"> sub</a></span> </p></td> 
  <td class="stentry"> <p>Selecione uma subárea do grupo ou objeto selecionado. </p></td> 
 </tr> 
</table>

