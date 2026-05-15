---
title: SpinView.iconeffect
description: SpinView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 473207d2-7e26-4ea3-940e-5a21f29a2b91
TQID: 'https://experienceleague.adobe.com/hZb5SQHHzH8zeR7UoxOp2Oc-MTWvvmGvsvc7mzsP40k'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 1%

---

# SpinView.iconeffect{#spinview-iconeffect}

` [SpinView.|<containerId>_spinView.]iconeffect=0|1[, *`contagem`*][, *`esmaecer`*][, *`autoHide`*]`

<table id="table_DF2137DF9C7441B381D2B03CEE4B880A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Habilita o iconeffect <span class="codeph"></span> para ser exibido na parte superior da imagem quando ela estiver em um estado de redefinição e sugerir uma ação disponível para interagir com a imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">contagem</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o número máximo de vezes que o <span class="codeph"> iconeffect</span> é exibido e reexibido. Um valor de <span class="codeph"> -1</span> indica que o ícone sempre reaparece indefinidamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fade</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica a duração da animação de exibição ou ocultação, em segundos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Define o número de segundos durante os quais <span class="codeph"> iconeffect</span> permanece totalmente visível antes de ser ocultado automaticamente. Ou seja, o tempo após a conclusão da animação de fade-in, mas antes do início da animação de fade-out. Uma configuração de <span class="codeph"> 0</span> desabilita o comportamento de ocultação automática. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,1,0.3,3`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
