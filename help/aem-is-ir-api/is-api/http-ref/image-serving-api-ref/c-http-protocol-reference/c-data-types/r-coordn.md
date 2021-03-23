---
description: Coordenadas normalizadas. Usado para especificar posições relativas em uma imagem, como deslocamentos de imagem ou parâmetros de corte, normalizadas para o tamanho da imagem.
seo-description: Coordenadas normalizadas. Usado para especificar posições relativas em uma imagem, como deslocamentos de imagem ou parâmetros de corte, normalizadas para o tamanho da imagem.
seo-title: cordN
solution: Experience Manager
title: cordN
uuid: e182650b-aff6-4dd2-8edb-cd0d361865fd
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---


# cordN{#coordn}

Coordenadas normalizadas. Usado para especificar posições relativas em uma imagem, como deslocamentos de imagem ou parâmetros de corte, normalizadas para o tamanho da imagem.

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>deslocamento de coordenada normalizado para o tamanho de uma imagem (real, real) </p></td> 
 </tr> 
</table>

Os valores positivos avançam para o canto inferior direito.

Em muitos casos, a posição de referência é o centro da imagem. Nesse caso, 0,0 corresponde ao centro da imagem, -0,5,-0,5 ao canto superior esquerdo e 0,5, 0,5 ao canto inferior direito.

Também usado para especificar tamanhos de imagem ou tamanho de retângulo em relação ao tamanho da camada 0. Nesse caso, os valores devem ser maiores que 0. 0 pode indicar que um valor padrão específico deve ser usado. 1,1 especifica um tamanho igual ao da camada 0.
