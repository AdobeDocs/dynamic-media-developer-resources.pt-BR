---
description: Habilita a otimização do FXG.
solution: Experience Manager
title: enableVisibleAttributeOtimization
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: a643694e-f6a2-424e-8f6e-3dbb4cdc41b3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 1%

---

# enableVisibleAttributeOtimization{#enablevisibleattributeoptimization}

Habilita a otimização do FXG.

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOtimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Remove os elementos cuja visibilidade é definida como false no FXG ao passar esse FXG, o que, por sua vez, reduz o tempo de processamento do FXG. Embora remova apenas os elementos com visibilidade como false, isso não afetaria nenhum outro elemento no FXG. Por exemplo, se houver texto em `Path` e a visibilidade de `Path` for definida como false, ele não será removido do FXG mesmo com esse modificador ativado, pois o texto precisa ser desenhado nesse caminho.

O padrão é 1.
