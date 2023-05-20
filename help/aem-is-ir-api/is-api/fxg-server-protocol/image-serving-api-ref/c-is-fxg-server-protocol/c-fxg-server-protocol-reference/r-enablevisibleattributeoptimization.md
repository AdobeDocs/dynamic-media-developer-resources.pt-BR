---
description: Permite a otimização de FXG.
solution: Experience Manager
title: enableVisibleAttributeOtimization
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a643694e-f6a2-424e-8f6e-3dbb4cdc41b3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 1%

---

# enableVisibleAttributeOtimization{#enablevisibleattributeoptimization}

Permite a otimização de FXG.

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOtimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Remove os elementos cuja visibilidade é definida como falsa no FXG ao transmitir este FXG, o que, por sua vez, reduz o tempo de processamento do FXG. Embora ela remova apenas os elementos com visibilidade igual a false que não afetariam nenhum outro elemento no FXG. Por exemplo, se houver texto em `Path` e visibilidade da `Path` for definido como false, ele não será removido do FXG mesmo com esse modificador ativado, pois o texto precisa ser desenhado nesse caminho.

O padrão é 1.
