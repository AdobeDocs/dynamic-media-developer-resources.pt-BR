---
title: camada
description: Selecione Camada. Seleciona uma camada e inicia um novo segmento de definição de camada na sequência de comandos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f1200d86-d88c-4990-ae36-2ce96ae94343
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# camada{#layer}

Selecione Camada. Seleciona uma camada e inicia um novo segmento de definição de camada na sequência de comandos.

`layer= *`n`*|comp[, *`nome`*]`

`layer= *`nome`*`

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
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nome</span></span> </p></td> 
  <td class="stentry"> <p>Nome da camada. </p></td> 
 </tr> 
</table>

Todos os comandos dentro do segmento de camada são aplicados à camada especificada. Um segmento de camada é terminado pelo próximo comando `layer=` ou `effect=` ou pelo fim da solicitação.

Especifique `layer=comp` para selecionar a imagem composta (ou exibição, para alguns comandos).

O número da camada especifica efetivamente a ordem z para a camada. As camadas com numeração mais alta são colocadas sobre camadas com numeração mais baixa.

Os números de camada não precisam ser consecutivos. Camada 0 é necessária.

Um nome pode ser atribuído a uma camada com a variante de comando `layer= *`n`*, *`name`*`. Depois que uma camada nomeada é definida, ela pode ser referenciada com ` layer= *`nome`*`, sem precisar saber o número da camada. Vários nomes podem ser atribuídos à mesma camada, usando vários comandos `layer= *`n`*, *`name`*`.

>[!NOTE]
>
>A Camada 0 determina o tamanho geral da tela de composição. Todas as partes das camadas que estão fora dos limites da camada 0 são cortadas quando o composto é construído.

## Propriedades {#section-499963ee52c14f2898f0d0f90c1d01be}

Camada. Não há suporte para referências de variável de substituição em `layer=`.

`comp` não é permitido como uma cadeia de caracteres *`name`*. Um erro será retornado se o mesmo *`name`* for atribuído a mais de uma camada, ou se uma camada for referenciada por *`name`*, que não foi definida anteriormente.

## Padrão {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. Muitos comandos e atributos se aplicam à camada 0 se `layer=comp`.

## Casos especiais {#section-e087cb2e3562473e8d391abfa3b9489f}

* Se o mesmo nome for mapeado para várias camadas (por exemplo: `layer=1,image&layer=2,image`), ocorrerá um erro.
* Se o mesmo nome for mapeado várias vezes para uma única camada (por exemplo: `layer=1,image&layer=1,image`), o escopo será definido como de costume, sem erros.
* Há suporte para vários nomes para a mesma camada.

  Qualquer nome pode ser usado para fazer referência à camada (por exemplo: `layer=1,image&layer=1,picture`).
* Se um nome referenciado nunca for mapeado para um número de camada (por exemplo: `layer=1,image&layer=picture`), ocorrerá um erro.
* Variáveis de substituição não têm suporte em modificadores de camada (por exemplo: `layer=$image$`).

  Isso se aplica a todas as permutações, não apenas aos nomes de camadas, mas aos modificadores de camadas em geral.

* Todas as regras de mesclagem e substituição devem funcionar exatamente como quando a mesma camada é referenciada em várias fontes (solicitação, registros de catálogo pré ou pós-modificador, macros e assim por diante).

## Exemplo {#section-cc40de6a0a754178aa752601539c815b}

Veja os exemplos em [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).
