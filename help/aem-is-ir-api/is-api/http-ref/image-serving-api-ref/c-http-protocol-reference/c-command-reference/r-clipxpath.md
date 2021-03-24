---
description: Caminho de recorte de camada invertido. Especifica um caminho de clipe de exclusão para a camada atual. Todas as partes da camada que estão dentro da área definida por clipXPath= são renderizadas de forma transparente.
solution: Experience Manager
title: clipXPath
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---


# clipXPath{#clipxpath}

Caminho de recorte de camada invertido. Especifica um caminho de clipe de exclusão para a camada atual. Todas as partes da camada que estão dentro da área definida por clipXPath= são renderizadas de forma transparente.

`clipXPath= *`pathDefinition`*`

`clipXPathE= *``*&#42;[, *`pathNameName`*]`

<table id="simpletable_27AFC3A694874CF8B673460820EFD90D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Dados do caminho. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span> </span> </p> </td> 
  <td class="stentry"> <p>Nome do caminho incorporado na imagem de origem da camada (somente ASCII). </p></td> 
 </tr> 
</table>

Consulte [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) para obter informações adicionais, incluindo uma descrição de `*`pathName`*` e `*`pathDefinition`*`.

## Propriedades {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Atributo de camada. Aplica-se à camada atual ou à imagem composta se `layer=comp`. Ignorado se `clipPath=` não for especificado. Ignorado por camadas de efeito.

## Padrão {#section-d1986aa31af14767aeb1b4a57add67f4}

Nenhum.

## Consulte também {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
