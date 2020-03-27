---
description: Manuseio de erros de seleção de separação. Especifica a ação a ser tomada se o comando sel= falhar porque o local do pixel especificado não está dentro da área de máscara de um objeto selecionável.
seo-description: Manuseio de erros de seleção de separação. Especifica a ação a ser tomada se o comando sel= falhar porque o local do pixel especificado não está dentro da área de máscara de um objeto selecionável.
seo-title: OnFailSel
solution: Experience Manager
title: OnFailSel
topic: Scene7 Image Serving - Image Rendering API
uuid: 073b6651-970c-460c-b044-e3ef37cc677a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# OnFailSel{#onfailsel}

Manuseio de erros de seleção de separação. Especifica a ação a ser tomada se o comando sel= falhar porque o local do pixel especificado não está dentro da área de máscara de um objeto selecionável.

## Propriedades {#section-cec491e6c5c744f9bfafaaa9d8774f83}

Enum.

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Herdar do <span class="codeph"> padrão::OnFailSel </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Manter a seleção anterior. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Desmarcar; quaisquer tentativas de aplicar um material ou mostrar/ocultar objetos serão ignoradas. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Retorna um erro. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Selecione o grupo padrão (o primeiro grupo na hierarquia de vinheta que contém objetos renderizáveis). </p> </td> 
 </tr> 
</table>

## Padrão {#section-c25f458f9f8f4236963a95779529e664}

Herdado de `default::OnFailSel` se não estiver definido.

## Consulte também {#section-f8b15dd64c674c5484d190dd9e3016af}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b) , [atributo::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
