---
description: Parâmetro comum a todos os visualizadores.
seo-description: Parâmetro comum a todos os visualizadores.
seo-title: initialFrame
solution: Experience Manager
title: initialFrame
topic: Dynamic media
uuid: 5d1c3a8a-8598-47c9-a106-36e8c6fcafb0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# initialFrame{#initialframe}

Parâmetro comum a todos os visualizadores.

>[!NOTE]
>
>Esse comando não se aplica ao Visualizador de imagens de vídeo.

` initialFrame= *`frameIdx`*[ *`,pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica um índice de quadros com base em zero que o visualizador exibe ao carregar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>Um índice com base em zero da página espelhada quando o dispositivo está na orientação retrato. Em um ambiente "da esquerda para a direita", <span class="codeph"> 0</span> significa "página da esquerda" e <span class="codeph"> 1</span> significa "página da direita". Na "direita para a esquerda" é o oposto: <span class="codeph"> 0</span> significa "página direita" e <span class="codeph"> 1</span> significa "página esquerda". </p> <p>Se não for especificado, <span class="codeph"> 0</span> será assumido por padrão. Ignorado quando o dispositivo está na orientação paisagem. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-10ee45d637134e0fbcd943c62578cb78}

Opcional.

## Padrão {#section-d411e450028c460392cb8508f8ccc5d9}

Sem padrão.

## Example {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```

