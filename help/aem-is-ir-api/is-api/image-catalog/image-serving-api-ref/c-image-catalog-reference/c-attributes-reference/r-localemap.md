---
description: Mapa de tradução de ID. Especifica as regras usadas para converter IDs de imagem genéricas em IDs específicas da localidade.
solution: Experience Manager
title: LocaleMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# LocaleMap{#localemap}

Mapa de tradução de ID. Especifica as regras usadas para converter IDs de imagem genéricas em IDs específicas da localidade.

`*`item`*&#42;['|' *`item`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> item</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>,<span class="varname"> locSuffix</span>*[','<span class="varname"> locSuffix</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locId</span> </p></td> 
  <td class="stentry"> <p>ID da localidade (não diferencia maiúsculas de minúsculas). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locSuffix</span> </p></td> 
  <td class="stentry"> <p>Sufixo do local. </p></td> 
 </tr> 
</table>

`LocaleMap` refere-se a um `locId` que pode ser mapeado para qualquer número de `locSuffix`.

Empty *`locSuffix`* valores são permitidos. *`locSuffix`* os valores devem ser classificados na ordem em que devem ser pesquisados. A primeira correspondência é retornada.

O Servidor de imagens pesquisa o *`locId`* valores para uma correspondência que não diferencia maiúsculas de minúsculas com o `locale=` valor especificado na solicitação. Se uma correspondência for encontrada, o primeiro associado *`locSuffix`* O valor de está anexado à id do catálogo original. Se esta entrada de catálogo existir, ela será usada, caso contrário, a próxima *`locSuffix`* é tentado. Se nenhuma das opções *`locSuffix`* valores corresponde a uma entrada de catálogo, o Servidor de imagens retorna um erro ou uma imagem padrão.

Um vazio *`locId`* o valor corresponde a vazio e desconhecido `locale=` strings. Isso permite definir uma regra padrão para localidades desconhecidas.

A conversão de ID, quando ativada, é aplicada a todas as IDs que fazem referência às entradas do catálogo de imagens e do catálogo de conteúdo estático.

## Propriedades {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

Um ou mais itens, separados por |, onde cada item consiste em dois ou mais valores de sequência separados por vírgulas. *`locId`* e `locale=` são comparados. Não diferencia maiúsculas de minúsculas.

## Consulte também {#section-19fba6d5be59439c8bf8ec7513c1a6da}

Suporte à localização, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
