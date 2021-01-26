---
description: Tamanho normalizado. Usado para especificar tamanhos de imagem ou tamanhos de retângulo, normalizado em relação ao tamanho da camada 0 ou de alguma outra imagem.
seo-description: Tamanho normalizado. Usado para especificar tamanhos de imagem ou tamanhos de retângulo, normalizado em relação ao tamanho da camada 0 ou de alguma outra imagem.
seo-title: sizeN
solution: Experience Manager
title: sizeN
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6fc05654-6f0d-499f-97bc-6b7134024e1f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# sizeN{#sizen}

Tamanho normalizado. Usado para especificar tamanhos de imagem ou tamanhos de retângulo, normalizado em relação ao tamanho da camada 0 ou de alguma outra imagem.

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>largura e altura normalizadas em relação a outra imagem (real, real, maior que 0) </p></td> 
 </tr> 
</table>

Ambos *nx* e *ny* têm de ser maiores que 0. 0,0 pode indicar que um tamanho padrão específico deve ser usado. 1,1 especifica um tamanho igual à imagem de referência.
