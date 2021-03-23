---
description: Atualiza o estado do contexto de publicação de um ativo.
seo-description: Atualiza o estado do contexto de publicação de um ativo.
seo-title: ContextStateUpdate
solution: Experience Manager
title: ContextStateUpdate
uuid: ef579d3c-1899-4088-903e-e6ed5a414ca8
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 0%

---


# ContextStateUpdate{#contextstateupdate}

Atualiza o estado do contexto de publicação de um ativo.

Sintaxe

## Parâmetros {#section-9f747df071854c6896fdbb95684ad947}

Defina o estado do contexto de publicação de um ativo com `setAssetsContextState`.

<table id="table_FD172CEA4EFE44E08ADA22D090DC06CA">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Nome </th>
   <th colname="col2" class="entry"> Tipo </th>
   <th colname="col3" class="entry"> Descrição </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> contextHandle</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:string </span></td>
   <td colname="col3"> Lidar com o contexto de publicação. </td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> publishState</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:string</span></td>
   <td colname="col3">O estado atualizado do ativo publicado para o contexto de publicação especificado. Inclui: 
    <ul id="ul_CF6019C4CA3648B687C252F1A7C2EAAF">
     <li id="li_4367D7A058F045D98CDF58009E2AC7BC"><span class="codeph"> MarkedForPublish</span></li>
     <li id="li_EEFC6A76C1014C6D9D5E66F271B68606"><span class="codeph"> NotMarkedForPublish</span></li>
     <li id="li_5145CFA39F5249C48DBD0A37543AF055"><span class="codeph"></span></li>
    </ul></td>
  </tr>
 </tbody>
</table>

>[!MORELIKETHIS]
>
>* [Estado de publicação](../../string-constants/c-string-constants/r-publish-state.md#reference-a9d80231514b4272b39d10c1a7aadca8)

