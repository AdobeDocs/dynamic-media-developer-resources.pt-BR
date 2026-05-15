---
title: coordN
description: Coordenadas Normalizadas. Usado para especificar posições relativas dentro de uma imagem, como deslocamentos de imagem ou parâmetros de corte, normalizadas para o tamanho da imagem.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
TQID: 'https://experienceleague.adobe.com/-dtYByOGK-mNAWc0yQBs4nu5sO1r-Ormq70iwdDZBjg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 155
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

Geralmente, a posição de referência é o centro da imagem. Nesse caso, `0,0` corresponde ao centro da imagem, `-0.5,-0.5` ao canto superior esquerdo e `0.5,0.5` ao canto inferior direito.

Também é usado para especificar o tamanho da imagem ou o tamanho do retângulo em relação ao tamanho da camada 0. Nesse caso, o valor deve ser maior que 0. 0 pode indicar que um valor padrão específico deve ser usado. Um valor de `1,1` especifica um tamanho igual ao da camada 0.
