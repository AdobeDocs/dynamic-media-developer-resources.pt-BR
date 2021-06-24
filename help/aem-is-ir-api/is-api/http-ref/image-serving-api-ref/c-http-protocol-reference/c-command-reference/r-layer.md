---
description: Selecione Camada. Seleciona uma camada e inicia um novo segmento de definição de camada na sequência de comandos.
solution: Experience Manager
title: camada
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: f1200d86-d88c-4990-ae36-2ce96ae94343
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# camada{#layer}

Selecione Camada. Seleciona uma camada e inicia um novo segmento de definição de camada na sequência de comandos.

`layer= *``*|comp[, *`name`*]`

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

Especifique `layer=comp` para selecionar a imagem composta (ou exibir, para alguns comandos).

O número da camada especifica efetivamente a ordem z da camada. As camadas com número mais alto são colocadas sobre as camadas com número mais baixo.

Os números de camada não precisam ser consecutivos. A camada 0 é necessária.

Um nome pode ser atribuído a uma camada com a variante de comando `layer= *`n`*, *`name`*`. Depois que uma camada nomeada é definida, ela pode ser referenciada com ` layer= *`name`*`, sem precisar saber o número da camada. Vários nomes podem ser atribuídos à mesma camada, usando vários comandos `layer= *`n`*, *`name`*`.

>[!NOTE]
>
>A camada 0 determina o tamanho geral da tela de composição. Todas as partes de camadas que se encontram fora dos limites da camada 0 são cortadas quando o compósito é construído.

## Propriedades {#section-499963ee52c14f2898f0d0f90c1d01be}

comando Camada. As referências da variável de substituição não são suportadas em `layer=`.

`comp` não é permitido como uma  *`name`* string. Um erro é retornado se o mesmo *`name`* for atribuído a mais de uma camada, ou se uma camada for referenciada por *`name`* que não tenha sido definida anteriormente.

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

Veja os exemplos em [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).
