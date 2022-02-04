---
title: SpinView.lockdirection
description: SpinView.lockdirection
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: e29ba926-9e0e-4ddd-9f76-408f8ab3b4ca
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 1%

---

# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Especifica se é permitido uma alteração na direção de rotação se houver um conjunto de rotação 2D. </p> <p>Quando definido como <span class="codeph"> 1 </span>, o componente identifica a direção de arrastar ou deslizar principal (horizontal versus vertical) no início do gesto. Depois disso, mantém essa direção até o final do gesto. Por exemplo, se o usuário iniciar um giro horizontal e decidir continuar seu gesto de arrastar em uma direção vertical, o componente não executará um giro vertical. Em vez disso, considera apenas o movimento horizontal do mouse ou do deslizamento. </p> <p>Um valor de <span class="codeph"> 0 </span> permite que um usuário altere a direção da rotação a qualquer momento durante o progresso do gesto. A configuração não terá efeito se o conjunto de rotação for 1D. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
