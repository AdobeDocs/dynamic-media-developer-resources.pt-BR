---
title: camada
description: Selecione Camada. Seleciona uma camada e inicia um novo segmento de definição de camada na sequência de comandos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f1200d86-d88c-4990-ae36-2ce96ae94343
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# camada{#layer}

Selecione Camada. Seleciona uma camada e inicia um novo segmento de definição de camada na sequência de comandos.

`layer= *`n`*|comp[, *`name`*]`

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

Todos os comandos no segmento de camada são aplicados à camada especificada. Um segmento de camada é finalizado pelo próximo `layer=` ou `effect=` ou o fim da solicitação.

Especificar `layer=comp` para selecionar a imagem composta (ou exibir, para alguns comandos).

O número da camada especifica efetivamente a ordem z da camada. As camadas com número mais alto são colocadas sobre as camadas com número mais baixo.

Os números de camada não precisam ser consecutivos. A camada 0 é necessária.

Um nome pode ser atribuído a uma camada com a `layer= *`n`*, *`name`*` variante de comando. Depois que uma camada nomeada é definida, ela pode ser referenciada com ` layer= *`name`*`, sem precisar saber o número da camada. Vários nomes podem ser atribuídos à mesma camada, usando vários `layer= *`n`*, *`name`*` comandos.

>[!NOTE]
>
>A camada 0 determina o tamanho geral da tela de composição. Todas as partes de camadas que se encontram fora dos limites da camada 0 são cortadas quando o compósito é construído.

## Propriedades {#section-499963ee52c14f2898f0d0f90c1d01be}

comando Camada. As referências da variável de substituição não são suportadas em `layer=`.

`comp` não é permitido como *`name`* string. Um erro é retornado se o mesmo *`name`* for atribuída a mais de uma camada ou se uma camada for referenciada por *`name`* que não foi definido anteriormente.

## Padrão {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. Muitos comandos e atributos se aplicam à camada 0 se `layer=comp`.

## Casos especiais {#section-e087cb2e3562473e8d391abfa3b9489f}

* Se o mesmo nome for mapeado para várias camadas (por exemplo: `layer=1,image&layer=2,image`), ocorre um erro.
* Se o mesmo nome for mapeado para uma única camada várias vezes (por exemplo: `layer=1,image&layer=1,image`), o escopo é definido como de costume, sem erros.
* Há suporte para vários nomes para a mesma camada.

   Qualquer nome pode ser usado para referenciar a camada (por exemplo: `layer=1,image&layer=1,picture`).
* Se um nome referenciado nunca for mapeado para um número de camada (por exemplo: `layer=1,image&layer=picture`), ocorre um erro.
* As variáveis de substituição não são compatíveis com modificadores de camada (por exemplo: `layer=$image$`).

   Isso se aplica a todas as permutas, não apenas a nomes de camadas, mas a modificadores de camada em geral.

* Todas as regras de mesclagem e substituição devem funcionar exatamente como quando a mesma camada é referenciada em várias fontes (solicitação, registros de catálogo pré ou pós modificador, macros, etc.).

## Exemplo {#section-cc40de6a0a754178aa752601539c815b}

Veja os exemplos em [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).
