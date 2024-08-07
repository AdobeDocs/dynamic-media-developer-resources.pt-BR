---
title: initialFrame
description: Parâmetro comum a todos os visualizadores.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db77edf0-e223-4f44-b83b-b6dbe5c1abd6
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '102'
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
