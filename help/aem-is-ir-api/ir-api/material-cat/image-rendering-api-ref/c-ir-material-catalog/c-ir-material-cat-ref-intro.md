---
description: Este documento descreve o catálogo de materiais para a Renderização de imagem do Dynamic Media.
solution: Experience Manager
title: Introdução
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1cdb9c45-329d-44df-92c3-8cba5b2b1339
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---

# Introdução{#introduction}

Este documento descreve o catálogo de materiais para a Renderização de imagem do Dynamic Media.

**Público-alvo**

Este documento destina-se a programadores experientes e desenvolvedores de sites que desejam aproveitar a Renderização de imagem do Dynamic Media para um site ou um aplicativo personalizado.

Presume-se que o leitor esteja familiarizado com a Criação e renderização de imagem do Dynamic Media, padrões e convenções gerais do protocolo HTTP e terminologia básica de geração de imagens.

**Convenções de documento**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Literal </p> </td> 
  <td class="stentry"> <p>Nas seções de sintaxe, o texto em itálico é literal; isso não se aplica ao espaço em branco e aos símbolos [ ] { } | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>Nas seções descritivas, o texto não em itálico entre aspas simples é literal. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> parâmetro </span> </p> </td> 
  <td class="stentry"> <p>Itálico indica uma variável ou parâmetro, a ser substituído por um valor real. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> attribute::Item </span> </p> </td> 
  <td class="stentry"> <p>Um nome com o prefixo 'attribute::' se refere a um atributo de catálogo de imagem. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> catálogo::Item </span> </td> 
  <td class="stentry"> <p>Um nome prefixado com "catálogo::" refere-se a um campo de dados do catálogo de materiais. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item </span> </p> </td> 
  <td class="stentry"> <p>Um nome com o prefixo 'icc::' se refere a um campo no mapa de perfil de cores ICC. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro::Item </span> </p> </td> 
  <td class="stentry"> <p>Um nome com o prefixo "macro::" refere-se a um campo na tabela de definição de macro. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> conjunto de regras::Item </span> </p> </td> 
  <td class="stentry"> <p>Um nome com o prefixo "ruleset::" refere-se a um elemento em um conjunto de regras de pré-processamento de URL. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> padrão::Item </span> </p> </td> 
  <td class="stentry"> <p>Um nome com o prefixo 'default::' se refere a um atributo do catálogo de imagens padrão. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> vinheta::Item </span> </p> </td> 
  <td class="stentry"> <p>Um nome com o prefixo "vinheta::" refere-se a um campo no mapa de vinheta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> opcional </span> ] </p> </td> 
  <td class="stentry"> <p>Os elementos de sintaxe opcionais são colocados por colchetes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> opcional </span> ] </p> </td> 
  <td class="stentry"> <p>O elemento de sintaxe opcional pode ser repetido nenhuma ou mais vezes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1 </span>| <span class="varname"> item2 </span> </p> </td> 
  <td class="stentry"> <p>Uma barra vertical indica que o item de sintaxe único à esquerda ou o item à direita podem ser usados. Exatamente um item deve ser selecionado. </p> </td> 
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
  <td class="stentry"> <p>Não é permitido espaço em branco (espaços ou tabulações) em solicitações HTTP. Este documento usa ocasionalmente espaços em branco entre os elementos sintáticos apenas para maior clareza. </p> </td> 
 </tr> 
</table>
