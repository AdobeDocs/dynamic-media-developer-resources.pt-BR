---
description: Este documento descreve o catálogo de materiais para a renderização de imagem do Dynamic Media.
seo-description: Este documento descreve o catálogo de materiais para a renderização de imagem do Dynamic Media.
seo-title: Introdução
solution: Experience Manager
title: Introdução
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 38da0561-7730-4170-bf29-02de325b3ad9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---


# Introdução{#introduction}

Este documento descreve o catálogo de materiais para a renderização de imagem do Dynamic Media.

**Audiência pretendida**

Este documento destina-se a programadores experientes e desenvolvedores de sites da Web que desejam utilizar a Renderização de imagem da Dynamic Media para um site ou aplicativo personalizado.

Pressupõe-se que o leitor esteja familiarizado com a criação e renderização de imagens da Dynamic Media, padrões e convenções gerais de protocolo HTTP e terminologia básica de geração de imagens.

**convenções de documento**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Literal </p> </td> 
  <td class="stentry"> <p>Nas seções de sintaxe, o texto não itálico é literal; isso não se aplica ao espaço em branco e aos símbolos [ ] { } | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>Em seções descritivas, o texto não itálico em aspas simples é literal. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> parâmetro  </span> </p> </td> 
  <td class="stentry"> <p>Itálico indica uma variável ou parâmetro, que deve ser substituído por um valor real. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> atributo::Item  </span> </p> </td> 
  <td class="stentry"> <p>Um nome prefixado com 'attribute::' refere-se a um atributo de catálogo de imagens. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> catálogo::Item  </span> </td> 
  <td class="stentry"> <p>Um nome prefixado com 'catálogo::' refere-se a um campo de dados de catálogo de materiais. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item  </span> </p> </td> 
  <td class="stentry"> <p>Um nome com prefixo 'icc::' refere-se a um campo no mapa de perfis de cor ICC. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro::Item  </span> </p> </td> 
  <td class="stentry"> <p>Um nome com o prefixo 'macro::' refere-se a um campo na tabela de definição de macro. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> conjunto de regras::Item  </span> </p> </td> 
  <td class="stentry"> <p>Um nome com o prefixo "conjunto de regras::" refere-se a um elemento em um conjunto de regras de pré-processamento de URL. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> padrão::Item  </span> </p> </td> 
  <td class="stentry"> <p>Um nome prefixado com 'default::' refere-se a um atributo do catálogo de imagens padrão. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> vinheta::Item  </span> </p> </td> 
  <td class="stentry"> <p>Um nome com prefixo 'vinheta::' refere-se a um campo no mapa de vinheta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> opcional </span> ] </p> </td> 
  <td class="stentry"> <p>Os elementos de sintaxe opcionais são delimitados por colchetes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> opcional </span> ] </p> </td> 
  <td class="stentry"> <p>O elemento de sintaxe opcional pode ser repetido nenhuma ou mais vezes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1  </span>|  <span class="varname"> número2  </span> </p> </td> 
  <td class="stentry"> <p>Uma barra vertical indica que o item de sintaxe único à esquerda ou o item à direita podem ser usados. Deve ser selecionado exatamente um item. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> grupo </span> } </p> </td> 
  <td class="stentry"> <p>As chaves são usadas para agrupar elementos de sintaxe. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> grupo </span> } </p> </td> 
  <td class="stentry"> <p>Os elementos de sintaxe dentro do grupo podem ser repetidos uma ou mais vezes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Espaço em branco. </p> </td> 
  <td class="stentry"> <p>Espaço em branco (espaços ou tabulações) não é permitido em solicitações HTTP. Este documento utiliza ocasionalmente espaços em branco entre elementos sintáticos apenas para maior clareza. </p> </td> 
 </tr> 
</table>

