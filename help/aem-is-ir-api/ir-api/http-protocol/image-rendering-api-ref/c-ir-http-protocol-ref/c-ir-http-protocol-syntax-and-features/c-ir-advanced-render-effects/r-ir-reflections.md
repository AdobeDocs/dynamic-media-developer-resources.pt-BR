---
description: As vinhetas podem ser criadas para incluir dados de reflexão quase 3D.
seo-description: As vinhetas podem ser criadas para incluir dados de reflexão quase 3D.
seo-title: Reflexões
solution: Experience Manager
title: Reflexões
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6d86f566-0f02-4304-8a6c-08b1a2e9c72e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---


# Reflexões{#reflections}

As vinhetas podem ser criadas para incluir dados de reflexão quase 3D.

Se assim for, são utilizados os seguintes atributos de material para definir as propriedades da superfície refletora do material:

<table id="table_8769C726A17E412FB41F7CB87690B1FE"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Atributo </p> </th> 
   <th class="entry"> <p>Descrição </p> </th> 
   <th class="entry"> <p>Padrão </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca" type="reference" format="dita" scope="local"> <span class="codeph"> brilho=</span> </a> </p> </td> 
   <td> <p>Brilho superficial </p> </td> 
   <td> <p>Da vinheta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glossmap=  </span> </a> </p> </td> 
   <td> <p>Variação de brilho (imagem em escala cinza) </p> </td> 
   <td> <p>Nenhum </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> bruxa=  </span> </a> </p> </td> 
   <td> <p>Rugosidade da superfície </p> </td> 
   <td> <p>40% </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> type=</span> </a> </p> </td> 
   <td> <p>Tipo de material </p> </td> 
   <td> <p>0 (desconhecido) </p> </td> 
  </tr> 
 </tbody> 
</table>

O renderizador ajusta o intervalo dos atributos `gloss=` e `rough=` de acordo com `type=`. Alguns tipos de materiais, como o tecido, são geralmente menos reflexivos do que os tipos de materiais, como pedra ou metal, e a mesma quantidade de brilho especificada para um resultará num efeito de reflexão diferente do outro. `gloss=`e as irregularidades têm uma gama bastante larga se não  `type=` for especificada ou se estiver definida como 0.

`glossmap=` pode ser usado para controlar o brilho de um material com base em pixel por pixel.
