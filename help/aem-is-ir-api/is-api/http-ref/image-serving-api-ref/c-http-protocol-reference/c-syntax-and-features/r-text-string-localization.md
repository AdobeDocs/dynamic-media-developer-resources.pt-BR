---
title: Localização da cadeia de caracteres de texto
description: A localização da sequência de caracteres de texto permite que os catálogos de imagem contenham várias representações específicas do local para o mesmo valor da sequência de caracteres.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---

# Localização da cadeia de caracteres de texto{#text-string-localization}

A localização da sequência de caracteres de texto permite que os catálogos de imagem contenham várias representações específicas do local para o mesmo valor da sequência de caracteres.

O servidor retorna ao cliente a representação correspondente à localidade especificada com `locale=`, evitando a localização no lado do cliente e permitindo que os aplicativos alternem as localidades simplesmente enviando o valor `locale=` apropriado com as solicitações de texto IS.

## Escopo {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

A localização da cadeia de caracteres de texto é aplicada a todos os elementos de cadeia de caracteres que incluem o token de localização ` ^loc= *`locId`*^` nos seguintes campos de catálogo:

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Campo de catálogo</b> </th> 
   <th class="entry"> <b>Elemento de cadeia de caracteres no campo</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::ImageSet </span> </p> </td> 
   <td> <p>Qualquer subelemento que contenha uma string traduzível (delimitada por qualquer combinação de separadores ',' ';' ':' e/ou o início/fim do campo). </p> <p> Um valor de cor <span class="codeph"> 0xrggbb </span> no início de um campo localizável é excluído da localização e passado sem modificação. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Mapa </span> </p> </td> 
   <td> <p>Qualquer valor de atributo entre aspas simples ou duplas, exceto os valores dos atributos <span class="codeph"> coords= </span> e <span class="codeph"> shape= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Destinos </span> </p> </td> 
   <td> <p>O valor de qualquer destino <span class="codeph">.*.label </span> e <span class="codeph"> target.Propriedade *.userdata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::UserData </span> </p> </td> 
   <td> <p>O valor de qualquer propriedade. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sintaxe de string {#section-d12320edf300409f8e17565b143acafc}

Os elementos *`string`* habilitados para localização no catálogo de imagens consistem em uma ou mais cadeias de caracteres localizadas, cada uma precedida por um token de localização.

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span> </span> </p> </td> 
  <td class="stentry"> <p>ID de localidade interna para a <span class="varname"> localizedString </span> seguindo este <span class="varname"> localizationToken </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString </span> </span> </p> </td> 
  <td class="stentry"> <p>Sequência de caracteres localizada. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString </span> </span> </p> </td> 
  <td class="stentry"> <p>Sequência de caracteres a ser usada para localidades desconhecidas. </p> </td> 
 </tr> 
</table>

*`locId`* deve ser ASCII e não pode incluir &#39;^&#39;.

O &#39;^&#39; pode ocorrer em qualquer lugar em substrings com ou sem codificação HTTP. O servidor corresponde todo o padrão *`localizationToken`* `^loc=locId^` para separar subsequências.

Os *`stringElements`*, que não incluem pelo menos um *`localizationToken`*, não são considerados para localização.

## O mapa de tradução {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` define as regras usadas pelo servidor para determinar qual *`localizedStrings`* retornar ao cliente. Consiste em uma lista de entradas *`locales`* (correspondendo aos valores especificados com `locale=`), cada uma com nenhuma ou mais IDs de localidade internas ( *`locId`*). Por exemplo:

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

Valores de *`locId`* vazios indicam que *`defaultString`* deve ser retornado, se disponível.

Consulte a descrição de `attribute::LocaleStrMap` para obter detalhes.

## O processo de tradução {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

Dado o exemplo de mapa de tradução acima e a solicitação `/is/image/myCat/myItem?req=&locale=nl`, o servidor primeiro procura por &quot; `nl`&quot; no mapa de localidade. A entrada correspondente `nl,N` indica que, para cada *`stringElement`*, o *`localizedString`* marcado com `^loc=N^` deve ser retornado. Se este *`localizationToken`* não estiver presente no *`stringElement`*, um valor vazio será retornado.

Digamos que `catalog::UserData` para `myCat/myItem` contém o seguinte (quebras de linha inseridas para maior clareza):

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

O servidor retornaria o seguinte em resposta à solicitação do exemplo:

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## Localidades desconhecidas {#section-26dfeefbd60345de94bbfeaaf7741223}

No exemplo acima, `attribute::LocaleStrMap` tem uma entrada com um valor *`locale`* vazio. O servidor usa essa entrada para manipular todos os valores de `locale=` que não estejam explicitamente especificados no mapa de conversão.

O mapa de tradução de exemplo especifica que, nesse caso, *`defaultString`* deve ser retornado, se disponível. Portanto, o seguinte será retornado se este mapa de tradução for aplicado à solicitação `/is/image/myCat/myItem?req=&locale=ja`:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## Exemplos {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**Famílias de idiomas**

Vários valores *`locId`* podem ser associados a cada *`locale`* no mapa de tradução. O motivo é que ela permite o suporte a variações específicas de país ou região (por exemplo, inglês dos EUA versus inglês do Reino Unido) para select *`stringElements`* enquanto lida com a maioria dos conteúdos com localidades de base comuns (por exemplo, inglês internacional).

Por exemplo, o suporte foi adicionado para inglês específico dos EUA ( `*`locId`* EUS`) e inglês específico do Reino Unido ( `*`locId`* EUK`), para oferecer suporte à ortografia alternativa ocasional. Se EUK ou EUS não existir, ele volta para E. Da mesma forma, variantes alemãs específicas da Áustria ( `DAT`) podem ser disponibilizadas onde necessário, ao retornar o alemão comum *`localizedStrings`* (marcado com `D`) na maior parte do tempo.

O `attribute::LocaleStrMap` seria semelhante a:

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

A tabela a seguir descreve a saída de algumas combinações de *`stringElement`* e *`locale`* representativas:

<table id="table_A6B67587C5F44B5E9CD0E7ED29A81198"> 
 <thead> 
  <tr> 
   <th class="entry"> <i>elementoDaCadeiaDeCaracteres</i> </th> 
   <th class="entry"> <i>localidade</i> </th> 
   <th class="entry"> <p>String de saída </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^Inglês^loc=D^Alemão </span> </p> </td> 
   <td> <p> en, en_us, en_uk </p> <p> de, de_at, de_de </p> <p>todos os outros </p> </td> 
   <td> <p>Inglês </p> <p>Alemão </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Austrian </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>todos os outros </p> </td> 
   <td> <p>Inglês </p> <p>Reino Unido - Inglês </p> <p>Alemão </p> <p>Austríaco </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> Para este exemplo, o DDE <span class="varname"> locId </span> não existe no atributo <span class="codeph">::LocaleStrMap </span> e, portanto, a subsequência de caracteres associada a este <span class="varname"> locId </span> nunca é retornada. </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>todos os outros </p> </td> 
   <td> <p>Inglês </p> <p>Inglês (EUA) </p> <p>Alemão </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
