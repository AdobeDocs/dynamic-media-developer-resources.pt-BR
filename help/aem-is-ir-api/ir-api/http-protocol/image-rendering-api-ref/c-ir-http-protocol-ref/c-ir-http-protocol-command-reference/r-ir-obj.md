---
description: Selecione o objeto por nome. Seleciona o grupo de vinheta especificado por nome e inicia um novo MSS.
seo-description: Selecione o objeto por nome. Seleciona o grupo de vinheta especificado por nome e inicia um novo MSS.
seo-title: obj
solution: Experience Manager
title: obj
uuid: 2fede992-6759-45bd-b2f1-36e2c791d536
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# obj{#obj}

Selecione o objeto por nome. Seleciona o grupo de vinheta especificado por nome e inicia um novo MSS.

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
  <td class="stentry"> <p>Nome do grupo ou caminho/nome. </p> </td> 
 </tr> 
</table>

Subgrupos ou objetos individuais podem ser selecionados usando um caminho de grupo totalmente qualificado (ou seja, especificando o nome do grupo de destino ou objeto precedido por todos os grupos pai, separado por / (barras).

Se nenhum grupo/objeto com o nome especificado for encontrado, a ação especificada em `attribute::OnObjFail` será executada.

## Propriedades {#section-9463b36e8ff74c81a70c7c2b58927430}

comando Seleção; Delimitador MSS. A seleção de objeto é persistente até que outro objeto seja selecionado, com `obj=` ou `sel=`.

Os caminhos e nomes de grupo/objeto não distinguem maiúsculas de minúsculas.

## Padrão {#section-0c322850512c4896bb551856a549440e}

O primeiro grupo na vinheta que contém objetos renderizáveis é selecionado automaticamente quando uma nova vinheta é aberta.

## Consulte também {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b),  [atributo::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
