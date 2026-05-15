---
title: FlyoutZoomView.tip
description: FlyoutZoomView.tip
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: df73235b-547e-4d47-aa76-1d2bd4aead9b
TQID: 'https://experienceleague.adobe.com/KJkYYAJzpCL1oSSZCOIDOQjzZ4igTS2ZBoruO-GM9mQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 0%

---

# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *`duração`*[, *`contagem`*][, *`desaparecimento`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duração</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica por quantos segundos o texto de dica é exibido antes de ser ocultado. Quando definida como <span class="codeph"> -1</span>, a mensagem será sempre exibida, mesmo se o usuário ativar a imagem suspensa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contagem</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica o número de vezes que o texto é exibido ao visualizar novas imagens no conjunto. Um valor de <span class="codeph"> -1</span> significa que o texto é sempre exibido ao visualizar qualquer imagem no conjunto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fade</span> </span> </p> </td> 
   <td colname="col2"> <p>Especifica a duração de uma animação de desaparecimento gradual que ocorre quando o texto aparece ou desaparece. Um valor de <span class="codeph"> 0</span> significa nenhuma transição de desaparecimento gradual. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Padrão {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,1,0.3`

## Exemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`tip=1,-1,0`
