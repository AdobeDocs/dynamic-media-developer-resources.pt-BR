---
description: SpinView.lockdirection
solution: Experience Manager
title: SpinView.lockdirection
topic: Dynamic Media
uuid: b46a3d78-e381-4351-a4f4-a228386df527
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 1%

---


# SpinView.lockdirection{#spinview-lockdirection}

`[SpinView.|<containerId>_spinView.]lockdirection=0|1`

<table id="table_18D47E7C6A2D4D68B94225CB621D5F7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Especifica se uma alteração na direção de rotação deve ser permitida no caso de um conjunto de rotação 2D. </p> <p>Quando definido como <span class="codeph"> 1 </span>, o componente identifica a direção de arrastar ou deslizar principal (horizontal versus vertical) no start do gesto. Depois disso, mantém essa direção até o gesto terminar. Por exemplo, se o usuário start uma rotação horizontal e decide continuar seu gesto de arrastar em uma direção vertical, o componente não executa uma rotação vertical; em vez disso, considera apenas o movimento horizontal do mouse ou deslize o dedo. </p> <p>Um valor de <span class="codeph"> 0 </span> permite que um usuário altere a direção de rotação a qualquer momento durante o progresso do gesto. A configuração não afeta se o conjunto de rotação for 1D. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`lockdirection=1`
