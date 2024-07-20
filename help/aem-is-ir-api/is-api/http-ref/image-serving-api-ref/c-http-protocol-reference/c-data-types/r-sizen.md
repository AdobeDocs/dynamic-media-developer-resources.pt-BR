---
description: Tamanho Normalizado. Usado para especificar tamanhos de imagem ou tamanhos de retângulo, normalizados em relação ao tamanho da camada 0 ou de alguma outra imagem.
solution: Experience Manager
title: sizeN
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58c2d7da-31fc-49d1-a404-2e4a66ff0e56
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# sizeN{#sizen}

Tamanho Normalizado. Usado para especificar tamanhos de imagem ou tamanhos de retângulo, normalizados em relação ao tamanho da camada 0 ou de alguma outra imagem.

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>largura e altura normalizadas em relação a outra imagem (real, real, maior que 0) </p></td> 
 </tr> 
</table>

*nx* e *ny* devem ser maiores que 0. 0,0 pode indicar que deve ser utilizado um tamanho predefinido específico. 1,1 especifica um tamanho igual à imagem de referência.
