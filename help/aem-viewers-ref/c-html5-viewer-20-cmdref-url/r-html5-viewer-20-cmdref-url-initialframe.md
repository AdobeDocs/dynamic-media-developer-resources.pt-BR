---
title: initialFrame
description: Parâmetro comum a todos os visualizadores.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db77edf0-e223-4f44-b83b-b6dbe5c1abd6
TQID: 'https://experienceleague.adobe.com/v4kG-OcDN3wmdHDClJHeLR8d2SNcMa5sRQo89Qwig4I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 0%

---

# initialFrame{#initialframe}

Parâmetro comum a todos os visualizadores.

>[!NOTE]
>
>Esse comando não se aplica ao Visualizador de imagem de vídeo.

` initialFrame= *`frameIdx`*[ *`,pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica um índice de quadro com base em zero que o visualizador exibe ao carregar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>Um índice baseado em zero da página espelhada quando o dispositivo está na orientação de retrato. Para um ambiente da "esquerda para a direita", <span class="codeph"> 0</span> significa "página esquerda" e <span class="codeph"> 1</span> significa "página direita". Para um ambiente da "direita para a esquerda", é oposto: <span class="codeph"> 0</span> significa "página direita" e <span class="codeph"> 1</span> significa "página esquerda". </p> <p>Se não especificado, <span class="codeph"> 0</span> é assumido como padrão. Ignorado quando o dispositivo está na orientação paisagem. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-10ee45d637134e0fbcd943c62578cb78}

Opcional.

## Padrão {#section-d411e450028c460392cb8508f8ccc5d9}

Nenhum padrão.

## Exemplo {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```
