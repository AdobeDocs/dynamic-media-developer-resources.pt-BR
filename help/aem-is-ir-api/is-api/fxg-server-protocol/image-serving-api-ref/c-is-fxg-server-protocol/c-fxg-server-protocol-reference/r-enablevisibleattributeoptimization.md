---
description: Permite a otimização de FXG.
solution: Experience Manager
title: enableVisibleAttributeOtimization
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a643694e-f6a2-424e-8f6e-3dbb4cdc41b3
TQID: 'https://experienceleague.adobe.com/QpFJklGLyM9-R9RfGfMQE0mypUKrs-L4g21yWtRyO10'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 96
ht-degree: 2%

---

# enableVisibleAttributeOtimization{#enablevisibleattributeoptimization}

Permite a otimização de FXG.

<table id="simpletable_FDE0D8786BC747AF87A336452500E695"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> &amp;enableVisibleAttributeOtimization</span> </p> </td> 
  <td class="stentry"> <p>0|1 </p></td> 
 </tr> 
</table>

Remove os elementos cuja visibilidade é definida como falsa no FXG ao transmitir este FXG, o que, por sua vez, reduz o tempo de processamento do FXG. Embora ela remova apenas os elementos com visibilidade igual a false que não afetariam nenhum outro elemento no FXG. Por exemplo, se houver texto em `Path` e a visibilidade de `Path` estiver definida como falsa, ele não será removido de FXG mesmo com esse modificador habilitado, pois o texto precisa ser desenhado nesse caminho.

O padrão é 1.
