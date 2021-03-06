---
title: Introdução
description: Este documento descreve o protocolo HTTP para renderização de imagem do Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c185e45b-a56c-4576-b05d-22cc0025a7c4
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# Introdução{#introduction}

Este documento descreve o protocolo HTTP para renderização de imagem do Dynamic Media.

Apenas são descritos os aspectos do protocolo que se encontram à disposição do público. O servidor pode suportar comandos adicionais que são reservados para uso pelo software cliente Dynamic Media.

**Público-alvo pretendido**

Este documento destina-se a programadores experientes e desenvolvedores de sites que desejam usar a Renderização de imagem do Dynamic Media para um site ou aplicativo personalizado.

Pressupõe-se que o leitor esteja familiarizado com a Criação e renderização de imagens do Dynamic Media, padrões e convenções gerais de protocolo HTTP e terminologia básica de geração de imagens.

**Convenções de documento**

<table id="simpletable_E96BA470B3CE4266A9E6ED0440A56C40"> 
 <tr class="strow"> 
  <td class="stentry"> <p>literal </p> </td> 
  <td class="stentry"> <p>Nas seções de sintaxe, o texto não itálico é literal; não se aplica ao espaço em branco e aos símbolos [ ] { } | *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>Nas seções descritivas, o texto não itálico entre aspas simples é literal. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> parâmetro </span> </p> </td> 
  <td class="stentry"> <p>Itálico indica uma variável ou parâmetro que deve ser substituído por um valor real. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> atributo::Item </span> </p> </td> 
  <td class="stentry"> <p>Um nome com prefixo 'attribute::' refere-se a um atributo de catálogo de imagens. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catálogo::Item </span> </p> </td> 
  <td class="stentry"> <p>Um nome com prefixo 'catalog:::' refere-se a um campo de dados de catálogo de materiais. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc:Item </span> </p> </td> 
  <td class="stentry"> <p>Um nome com o prefixo 'icc::' refere-se a um campo no mapa de perfil de cores ICC. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro::Item </span> </p> </td> 
  <td class="stentry"> <p>Um nome com o prefixo 'macro::' refere-se a um campo na tabela de definição de macro. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> conjunto de regras::Item </span> </p> </td> 
  <td class="stentry"> <p>Um nome com o prefixo "conjunto de regras::" refere-se a um elemento em um conjunto de regras de pré-processamento de URL. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> padrão::Item </span> </p> </td> 
  <td class="stentry"> <p>Um nome com prefixo 'padrão::' refere-se a um atributo do catálogo de imagens padrão. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="codeph"> vinheta::Item </span> </td> 
  <td class="stentry"> <p>Um nome com prefixo 'vinheta::' refere-se a um campo no mapa de vinheta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>[ <span class="varname"> opcional </span> ] </p> </td> 
  <td class="stentry"> <p>Os elementos de sintaxe opcionais são colocados por colchetes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*[ <span class="varname"> opcional </span> ] </p> </td> 
  <td class="stentry"> <p>O elemento opcional de sintaxe pode ser repetido nenhuma ou mais vezes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item1 </span>| <span class="varname"> item2 </span> </p> </td> 
  <td class="stentry"> <p>Uma barra vertical indica que o único item de sintaxe à esquerda ou o item à direita podem ser usados. Deve ser selecionado exatamente um item. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>{ <span class="varname"> grupo </span> } </p> </td> 
  <td class="stentry"> <p>As chaves são usadas para agrupar elementos de sintaxe. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>*{ <span class="varname"> grupo </span> } </p> </td> 
  <td class="stentry"> <p>Os elementos de sintaxe no grupo podem ser repetidos uma ou mais vezes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>espaço em branco </p> </td> 
  <td class="stentry"> <p>O espaço em branco (espaços ou tabulações) não é permitido em solicitações HTTP. Este documento usa ocasionalmente o espaço em branco entre elementos sintáticos apenas para maior clareza. </p> </td> 
 </tr> 
</table>

**Termos comuns**

** *`MSS`* ** Segmento de especificação de material: um conjunto de atributos de material entre dois comandos de seleção na solicitação.

** *`vignette`* ** Uma imagem preparada na Criação de imagem do Dynamic Media para uso com a Renderização de imagem.
