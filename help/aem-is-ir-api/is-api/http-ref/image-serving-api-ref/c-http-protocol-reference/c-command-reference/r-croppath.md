---
description: Permite cortar para a caixa delimitadora de um caminho nomeado incorporado. Esse corte, por sua vez, altera o tamanho da imagem.
seo-description: Permite cortar para a caixa delimitadora de um caminho nomeado incorporado. Esse corte, por sua vez, altera o tamanho da imagem.
seo-title: cropPathE
solution: Experience Manager
title: cropPathE
uuid: 4689fd20-dfa0-47eb-8184-cd233f1ac088
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---


# cropPathE{#croppathe}

Permite cortar para a caixa delimitadora de um caminho nomeado incorporado. Esse corte, por sua vez, altera o tamanho da imagem.

`cropPathE= *``*&#42;[, *`pathNameName`*]`

<table id="table_598304852E844456AB3AC9FF1F178B71"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pathName</span></span> </p> </td> 
   <td colname="col2"> <p>Nome do caminho incorporado na imagem de origem da camada (somente ASCII). </p> <p> <span class="codeph"><span class="varname"> </span></span> pathName é o nome de um caminho incorporado na imagem de origem da camada. O caminho é automaticamente transformado conforme necessário para manter o alinhamento relativo com o conteúdo da imagem. Se mais de um <span class="codeph"><span class="varname"> pathName</span></span> for especificado, o servidor será dividido na caixa delimitadora de cada caminho, um de cada vez. Qualquer <span class="codeph"><span class="varname"> pathName</span></span> não encontrado na imagem de origem é ignorado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-acf7272ba93a4bbba818b8e6aa4dcea5}

Atributo de camada. Aplica-se à camada atual ou à imagem composta se `layer=comp`. Ignorado por camadas de efeito.

`cropPathE=` é ignorada se nenhum caminho com o nome especificado for encontrado na imagem de origem da camada ou se a origem da camada não for uma imagem.

## Padrão {#section-d1986aa31af14767aeb1b4a57add67f4}

Nenhum, para nenhum corte adicional da camada.

## Consulte também {#section-a60f6e37ebf14e458519fcc4d2cc911d}

[cortar](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab),  [clipPathE](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)
