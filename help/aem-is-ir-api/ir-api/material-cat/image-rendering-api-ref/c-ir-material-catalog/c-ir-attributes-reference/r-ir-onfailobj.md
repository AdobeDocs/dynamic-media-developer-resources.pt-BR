---
description: Tratamento de erros na seleção de objetos. Especifica a ação a ser executada se o comando obj= falhar porque o caminho especificado não pode ser correspondido na hierarquia do objeto de vinheta.
seo-description: Tratamento de erros na seleção de objetos. Especifica a ação a ser executada se o comando obj= falhar porque o caminho especificado não pode ser correspondido na hierarquia do objeto de vinheta.
seo-title: OnFailObj
solution: Experience Manager
title: OnFailObj
uuid: b9dcaf29-ffa5-47db-9c8c-d1809da73582
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 3%

---


# OnFailObj{#onfailobj}

Tratamento de erros na seleção de objetos. Especifica a ação a ser executada se o comando obj= falhar porque o caminho especificado não pode ser correspondido na hierarquia do objeto de vinheta.

## Propriedades {#section-2c779d9c133a443d9f0aed9fde7b703c}

Enum.

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Herdar de <span class="codeph"> padrão::OnFailObj </span>. </p> </td> 
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

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) ,  [atributo::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
