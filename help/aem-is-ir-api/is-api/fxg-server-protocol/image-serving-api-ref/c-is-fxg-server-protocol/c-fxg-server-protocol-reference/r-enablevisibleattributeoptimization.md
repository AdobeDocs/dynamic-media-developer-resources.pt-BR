---
description: Permite a otimização do FXG.
seo-description: Permite a otimização do FXG.
seo-title: enableVisibleAttributeOization
solution: Experience Manager
title: enableVisibleAttributeOization
topic: Scene7 Image Serving - Image Rendering API
uuid: 7f79aa12-6364-4b34-b547-88d4a778c015
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# enableVisibleAttributeOization{#enablevisibleattributeoptimization}

Permite a otimização do FXG.

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Remove os elementos cuja visibilidade é definida como false no FXG ao passar por esse FXG, o que, por sua vez, reduz o tempo de processamento do FXG. Embora remova apenas os elementos com visibilidade como falsos que não afetariam nenhum outro elemento no FXG. Por exemplo, se houver texto em `Path` e a visibilidade de `Path` estiver definida como falsa, ela não será removida do FXG mesmo com esse modificador ativado, pois o texto precisa ser desenhado nesse caminho.

O padrão é 1.
