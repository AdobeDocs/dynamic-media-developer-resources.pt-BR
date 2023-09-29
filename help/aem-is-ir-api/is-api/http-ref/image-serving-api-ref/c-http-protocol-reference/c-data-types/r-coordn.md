---
title: coordN
description: Coordenadas Normalizadas. Usado para especificar posições relativas dentro de uma imagem, como deslocamentos de imagem ou parâmetros de corte, normalizadas para o tamanho da imagem.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# coordN{#coordn}

Coordenadas Normalizadas. Usado para especificar posições relativas dentro de uma imagem, como deslocamentos de imagem ou parâmetros de corte, normalizadas para o tamanho da imagem.

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>deslocamento de coordenadas normalizado para o tamanho de uma imagem (real, real) </p></td> 
 </tr> 
</table>

Os valores positivos se movem em direção ao canto inferior direito.

Geralmente, a posição de referência é o centro da imagem. Nesse caso, `0,0` corresponde ao centro da imagem, `-0.5,-0.5` no canto superior esquerdo e `0.5,0.5` para o canto inferior direito.

Também é usado para especificar o tamanho da imagem ou o tamanho do retângulo em relação ao tamanho da camada 0. Nesse caso, o valor deve ser maior que 0. 0 pode indicar que um valor padrão específico deve ser usado. Um valor de `1,1` especifica um tamanho igual ao da camada 0.
