---
title: obj
description: Selecione o objeto por nome. Seleciona o grupo de vinhetas especificado por nome e inicia um novo MSS.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 17387203-f7a7-4876-a15b-2084894f981d
TQID: 'https://experienceleague.adobe.com/te9iyNajxDfgvHqqThbVUc7tBItxfMtxhOMl2eCLOsk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 0%

---

# obj{#obj}

Selecione o objeto por nome. Seleciona o grupo de vinhetas especificado por nome e inicia um novo MSS.

` obj= *`nome`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> nome </span> </span> </p> </td> 
  <td class="stentry"> <p>Nome do grupo ou caminho/nome. </p> </td> 
 </tr> 
</table>

Subgrupos ou objetos individuais podem ser selecionados usando um caminho de grupo totalmente qualificado (isto é, especificando o nome do grupo alvo ou objeto precedido por todos os grupos pai, separados por / (barras).

Se nenhum grupo/objeto com o nome especificado for encontrado, a ação especificada em `attribute::OnObjFail` será executada.

## Propriedades {#section-9463b36e8ff74c81a70c7c2b58927430}

Comando de seleção; delimitador de MSS. A seleção de objeto é persistente até que outro objeto seja selecionado, com `obj=` ou `sel=`.

Os caminhos e os nomes de grupo/objeto não fazem distinção entre maiúsculas e minúsculas.

## Padrão {#section-0c322850512c4896bb551856a549440e}

O primeiro grupo na vinheta que contém objetos renderizáveis é selecionado automaticamente quando uma nova vinheta é aberta.

## Consulte também {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b), [attribute::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)

