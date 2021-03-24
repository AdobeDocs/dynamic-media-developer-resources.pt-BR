---
description: Habilita a otimização do FXG.
solution: Experience Manager
title: enableVisibleAttributeOtimization
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

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
