---
description: Tamanho normalizado. Usado para especificar tamanhos de imagem ou tamanhos de retângulo, normalizado em relação ao tamanho da camada 0 ou de alguma outra imagem.
seo-description: Tamanho normalizado. Usado para especificar tamanhos de imagem ou tamanhos de retângulo, normalizado em relação ao tamanho da camada 0 ou de alguma outra imagem.
seo-title: sizeN
solution: Experience Manager
title: sizeN
uuid: 6fc05654-6f0d-499f-97bc-6b7134024e1f
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '117'
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

*nx* e *ny* devem ser maiores que 0. 0,0 pode indicar que deve ser usado um tamanho padrão específico. 1,1 especifica um tamanho igual à imagem de referência.
