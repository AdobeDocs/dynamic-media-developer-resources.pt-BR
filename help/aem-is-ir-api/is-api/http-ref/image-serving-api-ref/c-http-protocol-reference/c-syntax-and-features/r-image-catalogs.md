---
description: Os recursos e a sintaxe dos catálogos de imagens estão descritos nesta seção.
solution: Experience Manager
title: Catálogos de imagens
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---


# Catálogos de imagem{#image-catalogs}

Os recursos e a sintaxe dos catálogos de imagens estão descritos nesta seção.

Os catálogos de imagens oferecem os seguintes recursos:

* Permitir associação persistente de imagens com determinados metadados e comandos modificadores.

   As entradas em catálogos de imagens são referenciadas usando uma notação de atalho `*`rootId/objId`*`, onde `*`rootId`*` identifica o catálogo de imagens e `*`objId`*` identifica um registro de dados no catálogo.
* Forneça padrões para determinados atributos de solicitação, como a qualidade JPEG ou se uma marca d&#39;água deve ser aplicada.
* Gerenciar fontes, perfis ICC, definições de macro e modelos de solicitação

Mesmo se nenhum catálogo de imagem específico for definido, todos os recursos dos catálogos de imagem estarão disponíveis por meio do catálogo padrão ( [!DNL default.ini]).

Se `*`rootId`*` no caminho do URL da solicitação corresponder a `attribute::RootId` de um catálogo de imagem específico, esse catálogo se tornará o catálogo principal desta solicitação. O catálogo principal fornece os atributos e as configurações padrão para toda a solicitação. Se nenhuma correspondência for encontrada, o catálogo padrão será usado.

Um catálogo identificado em um comando `src=` ou `mask=` fornece os seguintes atributos e dados de catálogo para a camada atual:

<table id="table_D3FA66EA5D054745900DE5A120885AA8"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Atributo/Dados</b> </th> 
   <th class="entry"> <b> Notas</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::DefaultExt</span> </p> </td> 
   <td> <p> a extensão padrão para todos os caminhos de arquivo de imagem na camada atual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::Expiration</span> </p> </td> 
   <td> <p> padrão para catálogo <span class="codeph">::Expiration</span> ou expiração da camada atual se nenhum registro de catálogo estiver envolvido </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::Icc*</span> </p> </td> 
   <td> <p> o perfil de cores ICC de trabalho, a intenção de renderização e o sinalizador de compensação de pontos negros para a solicitação e/ou a camada atual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::RootPath</span> </p> </td> 
   <td> <p> usado para todos os caminhos de arquivo de origem da camada atual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> atributo::Resolution</span> </p> </td> 
   <td> <p> padrão para catálogo <span class="codeph">::Resolution</span> somente </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo:Âncora</span> </p> </td> 
   <td> <p> padrão para o valor <span class="codeph"> anchor=</span> da camada atual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Expiration</span> </p> </td> 
   <td> <p> o menor valor de expiração de todas as camadas é usado como o valor de tempo de vida da imagem de resposta </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::IccProfile</span> </p> </td> 
   <td> <p> o perfil de cores da imagem de origem da camada atual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Mapa</span> </p> </td> 
   <td> <p> os dados do mapa de imagem para a camada atual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::MaskPath</span> </p> </td> 
   <td> <p> padrão para <span class="codeph"> mask=</span> para a camada atual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo:Modificador</span> </p> </td> 
   <td> <p> os comandos de prefixo da camada atual (cada comando no <span class="codeph"> catalog::Modifier</span> pode ser substituído pelo mesmo comando no URL, se especificado para a mesma camada) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Caminho</span> </p> </td> 
   <td> <p> o arquivo de imagem de origem da camada atual </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::PostModifier</span> </p> </td> 
   <td> <p> comandos postfix para a camada atual (semelhante a <span class="codeph"> catalog::Modifier</span>, mas comandos em <span class="codeph"> catalog::PostModifier</span> substituem os mesmos comandos especificados no URL ou em <span class="codeph"> catalog::Modifier</span>) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catálogo::Resolução</span> </p> </td> 
   <td> <p> a resolução do objeto da camada atual </p> </td> 
  </tr> 
 </tbody> 
</table>

Na mesma camada, `src=` e `mask=` devem fazer referência ao mesmo catálogo de imagem (se houver).

Um catálogo identificado em um comando `icc=` é usado apenas para procurar uma entrada da tabela de perfil ICC do catálogo. Nenhum outro atributo ou dado de catálogo está envolvido.

Se, `*`rootId`*` resolver um catálogo e `*`objId`*` for correspondido por um `catalog::Id` neste catálogo, então `*`rootId/objId`*` será efetivamente substituído pela entrada do catálogo, algo como isto:

`src=attribute::RootPath/catalog::Path& mask=attribute::RootPath/catalog::MaskPath& anchor=catalog::Anchor& catalog::Modifier& catalog::PostModifier`

## Consulte também {#section-00e4f6b39cd14244bcce537a3f831259}

[Referência](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) do catálogo de imagens,  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [âncora=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
