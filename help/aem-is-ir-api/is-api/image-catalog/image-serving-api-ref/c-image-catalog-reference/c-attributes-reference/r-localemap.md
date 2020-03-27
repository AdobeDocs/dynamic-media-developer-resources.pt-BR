---
description: Mapa de tradução de ID. Especifica as regras usadas para converter IDs de imagem genéricas em IDs específicas da localidade.
seo-description: Mapa de tradução de ID. Especifica as regras usadas para converter IDs de imagem genéricas em IDs específicas da localidade.
seo-title: LocaleMap
solution: Experience Manager
title: LocaleMap
topic: Scene7 Image Serving - Image Rendering API
uuid: 3609a595-2948-43a4-ba8c-fd1a9ea4e26e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# LocaleMap{#localemap}

Mapa de tradução de ID. Especifica as regras usadas para converter IDs de imagem genéricas em IDs específicas da localidade.

` *`item`*&#42;['|' *`item`*]`

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
  <td class="stentry"> <p>Sufixo da localidade. </p></td> 
 </tr> 
</table>

`LocaleMap` refere-se a um `locId` que pode ser mapeado para qualquer número de `locSuffix`.

São permitidos *`locSuffix`* valores vazios. *`locSuffix`* devem ser classificados na ordem em que devem ser pesquisados. A primeira correspondência é retornada.

O Serviço de imagem pesquisa os *`locId`* valores para uma correspondência que não diferencia maiúsculas de minúsculas com o `locale=` valor especificado na solicitação. Se uma correspondência for encontrada, o primeiro *`locSuffix`* valor associado será anexado à ID do catálogo original. Se esta entrada de catálogo existir, ela será usada, caso contrário, o próximo *`locSuffix`* valor será tentado. Se nenhum dos *`locSuffix`* valores corresponder a uma entrada de catálogo, o Serviço de imagem retornará um erro ou uma imagem padrão.

Um *`locId`* valor vazio corresponde a `locale=` sequências de caracteres vazias e desconhecidas. Isso permite definir uma regra padrão para localidades desconhecidas.

A tradução da ID, quando ativada, é aplicada a todas as ids que fazem referência ao catálogo de imagens e às entradas do catálogo de conteúdo estático.

## Propriedades {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

Um ou mais itens, separados por|, em que cada item consiste em dois ou mais valores de sequência separados por vírgulas. *`locId`* e `locale=` são comparados. Não diferencia maiúsculas de minúsculas.

## Consulte também {#section-19fba6d5be59439c8bf8ec7513c1a6da}

Suporte à Localização, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [atributo::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
