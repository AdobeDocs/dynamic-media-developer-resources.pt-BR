---
description: Selecione Camada. Seleciona uma camada e start um novo segmento de definição de camada na sequência de comandos.
seo-description: Selecione Camada. Seleciona uma camada e start um novo segmento de definição de camada na sequência de comandos.
seo-title: camada
solution: Experience Manager
title: camada
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 882309b3-51d7-477e-bd09-068ce9e55eb5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 0%

---


# layer{#layer}

Selecione Camada. Seleciona uma camada e start um novo segmento de definição de camada na sequência de comandos.

`layer= *``*|comp[, *`nome`*]`

`layer= *`name`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>Número de camadas a serem selecionadas (0 ou maior int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> comp</span> </p></td> 
  <td class="stentry"> <p>Selecione a imagem composta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p></td> 
  <td class="stentry"> <p>Nome da camada. </p></td> 
 </tr> 
</table>

Todos os comandos no segmento de camada são aplicados à camada especificada. Um segmento de camada é encerrado pelo próximo comando `layer=` ou `effect=` ou pelo final da solicitação.

Especifique `layer=comp` para selecionar a imagem composta (ou visualização, para alguns comandos).

O número da camada especifica efetivamente a ordem z da camada. As camadas com numeração mais alta são colocadas sobre as camadas com numeração mais baixa.

Os números de camada não precisam ser consecutivos. A camada 0 é obrigatória.

Um nome pode ser atribuído a uma camada com a variante de comando `layer= *`n`*, *`name`*`. Depois que uma camada nomeada é definida, ela pode ser referenciada com ` layer= *`name`*`, sem precisar saber o número da camada. Vários nomes podem ser atribuídos à mesma camada, usando vários comandos `layer= *`n`*, *`name`*`.

>[!NOTE]
>
>A camada 0 determina o tamanho geral da tela de composição. Todas as partes de camadas que se encontram fora dos limites da camada 0 são cortadas quando o composto é construído.

## Propriedades {#section-499963ee52c14f2898f0d0f90c1d01be}

comando Camada. Referências de variáveis de substituição não são suportadas em `layer=`.

`comp` não é permitido como uma  *`name`* string. Um erro será retornado se o mesmo *`name`* for atribuído a mais de uma camada, ou se uma camada for referenciada por *`name`* que não foi definida anteriormente.

## Padrão {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. Muitos comandos e atributos se aplicam à camada 0 se `layer=comp`.

## Casos especiais {#section-e087cb2e3562473e8d391abfa3b9489f}

* Se o mesmo nome for mapeado para várias camadas (por exemplo: `layer=1,image&layer=2,image`), ocorre um erro.
* Se o mesmo nome for mapeado para uma única camada várias vezes (por exemplo: `layer=1,image&layer=1,image`), o escopo é definido como de costume, sem erros.
* Vários nomes para a mesma camada são suportados.

   Qualquer nome pode ser usado para fazer referência à camada (por exemplo: `layer=1,image&layer=1,picture`).
* Se um nome referenciado nunca for mapeado para um número de camada (por exemplo: `layer=1,image&layer=picture`), ocorre um erro.
* As variáveis de substituição não são suportadas em modificadores de camada (por exemplo: `layer=$image$`).

   Isso se aplica a todas as permutações, não apenas aos nomes de camadas, mas aos modificadores de camadas em geral.

* Todas as regras de mesclagem e substituição devem funcionar exatamente como quando a mesma camada é referenciada em várias fontes (registros de catálogo de pré ou pós modificadores, macros etc.).

## Exemplo {#section-cc40de6a0a754178aa752601539c815b}

Consulte os exemplos em [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).
