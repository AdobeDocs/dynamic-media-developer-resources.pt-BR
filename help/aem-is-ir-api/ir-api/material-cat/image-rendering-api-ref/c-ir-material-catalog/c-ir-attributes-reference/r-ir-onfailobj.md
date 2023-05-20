---
title: NoObjFalha
description: Tratamento de erros de seleção de objetos. Especifica a ação a ser tomada se o comando obj= falhar porque o caminho especificado não pode ser correspondido na hierarquia de objetos de vinheta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0ed04daf-1797-4c12-ae6d-a9a008de9d1d
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 4%

---

# NoObjFalha{#onfailobj}

Tratamento de erros de seleção de objetos. Especifica a ação a ser tomada se o comando obj= falhar porque o caminho especificado não pode ser correspondido na hierarquia de objetos de vinheta.

## Propriedades {#section-2c779d9c133a443d9f0aed9fde7b703c}

Enum.

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Herdar de <span class="codeph"> default::OnFailObj </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Manter a seleção anterior. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Desmarcar; qualquer tentativa de aplicar um material ou mostrar/ocultar objetos será ignorada. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Retorne um erro. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Selecione o grupo padrão (o primeiro grupo na hierarquia de vinheta que contém objetos renderizáveis). </p> </td> 
 </tr> 
</table>

## Padrão {#section-a5a95a2b4a204a4eae350e5b544d1513}

Herdado de `default::OnFailObj` se não estiver definido.

## Consulte também {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [attribute::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
