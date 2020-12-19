---
description: Caminho do clipe de camada invertido. Especifica um caminho de clipe de exclusão para a camada atual. Todas as partes da camada que estão dentro da área definida por clipXPath= são renderizadas de forma transparente.
seo-description: Caminho do clipe de camada invertido. Especifica um caminho de clipe de exclusão para a camada atual. Todas as partes da camada que estão dentro da área definida por clipXPath= são renderizadas de forma transparente.
seo-title: clipXPath
solution: Experience Manager
title: clipXPath
topic: Scene7 Image Serving - Image Rendering API
uuid: a4062f3f-5dba-4514-acde-e1b7d608a2e9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# clipXPath{#clipxpath}

Caminho do clipe de camada invertido. Especifica um caminho de clipe de exclusão para a camada atual. Todas as partes da camada que estão dentro da área definida por clipXPath= são renderizadas de forma transparente.

`clipXPath= *`pathDefinition`*`

`clipXPathE= *``*&#42;[, *`pathNamePathName`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Dados de caminho. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span> </span> </p> </td> 
  <td class="stentry"> <p>Nome do caminho incorporado na imagem de origem da camada (somente ASCII). </p></td> 
 </tr> 
</table>

Consulte [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) para obter informações adicionais, incluindo uma descrição de ` *`pathName`*` e ` *`pathDefinition`*`.

## Propriedades {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Atributo de camada. Aplica-se à camada atual ou à imagem composta se `layer=comp`. Ignorado se `clipPath=` não for especificado. Ignorado pelas camadas de efeito.

## Padrão {#section-d1986aa31af14767aeb1b4a57add67f4}

Nenhum.

## Consulte também {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
