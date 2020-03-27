---
description: Tamanho normalizado. Usado para especificar tamanhos de imagem ou tamanhos de retângulo, normalizado em relação ao tamanho da camada 0 ou de alguma outra imagem.
seo-description: Tamanho normalizado. Usado para especificar tamanhos de imagem ou tamanhos de retângulo, normalizado em relação ao tamanho da camada 0 ou de alguma outra imagem.
seo-title: sizeN
solution: Experience Manager
title: sizeN
topic: Scene7 Image Serving - Image Rendering API
uuid: 6fc05654-6f0d-499f-97bc-6b7134024e1f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# sizeN{#sizen}

Tamanho normalizado. Usado para especificar tamanhos de imagem ou tamanhos de retângulo, normalizado em relação ao tamanho da camada 0 ou de alguma outra imagem.

<table id="simpletable_BB36205775D4447084E527E2630D28B9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>largura e altura normalizadas em relação a outra imagem (real, real, maior que 0) </p></td> 
 </tr> 
</table>

Tanto *nx* quanto *ny* devem ser maiores que 0. 0,0 pode indicar que um tamanho padrão específico deve ser usado. 1,1 especifica um tamanho igual à imagem de referência.
