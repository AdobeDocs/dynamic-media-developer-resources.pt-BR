---
description: Esse documento usa as seguintes convenções.
seo-description: Esse documento usa as seguintes convenções.
seo-title: convenções de Documento
solution: Experience Manager
title: convenções de Documento
topic: Scene7 Image Serving - Image Rendering API
uuid: c929774b-8560-4f8a-98fd-1b75d4419c4d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# convenções de Documento{#document-conventions}

Esse documento usa as seguintes convenções.

<table id="simpletable_8C9DB0DA5F2B4C068794415602B768CB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>literal </p> </td> 
  <td class="stentry"> <p>Nas seções de sintaxe, o texto não itálico é literal; isso não se aplica ao espaço em branco e aos símbolos [ ] { }| *. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>'literal' </p> </td> 
  <td class="stentry"> <p>Em seções descritivas, o texto não itálico em aspas simples é literal. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> parâmetro </span> </p> </td> 
  <td class="stentry"> <p>Itálico indica uma variável ou parâmetro, que deve ser substituído por um valor real. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> command= </span> </p> </td> 
  <td class="stentry"> <p>Um nome com um '=' à direita refere-se a um comando de protocolo HTTP de disponibilização de imagem. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> atributo::Item </span> </p> </td> 
  <td class="stentry"> <p>Um nome prefixo com <span class="codeph"> atributo: </span> refere-se a um atributo de catálogo de imagens. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catálogo::Item </span> </p> </td> 
  <td class="stentry"> <p>Um nome com prefixo no <span class="codeph"> catálogo: </span> refere-se a um campo de dados do catálogo de imagens. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> icc::Item </span> </p> </td> 
  <td class="stentry"> <p>Um nome com prefixo <span class="codeph"> icc: </span> refere-se a um campo no mapa de perfis de cores ICC. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> fonte::Item </span> </p> </td> 
  <td class="stentry"> <p>Um nome com prefixo de <span class="codeph"> fonte: </span> refere-se a um campo no mapa de fontes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> macro: Item </span> </p> </td> 
  <td class="stentry"> <p>Um nome prefixo com <span class="codeph"> macro: </span> refere-se a um campo na tabela de definição de macro. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> conjunto de regras::Item </span> </p> </td> 
  <td class="stentry"> <p>Um nome com prefixo com <span class="codeph"> conjunto de regras: </span> refere-se a um elemento em um conjunto de regras de pré-processamento de URL. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> padrão::Item </span> </p> </td> 
  <td class="stentry"> <p>Um nome prefixo com <span class="codeph"> padrão: </span> refere-se a um atributo do catálogo de imagens padrão. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> [ <span class="varname"> opcional </span>] </span> </p> </td> 
  <td class="stentry"> <p>Os elementos de sintaxe opcionais são delimitados por colchetes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *[ <span class="varname"> opcional </span>] </span> </p> </td> 
  <td class="stentry"> <p>O elemento <span class="varname"> </span> de sintaxe opcional pode ser repetido nenhuma ou mais vezes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item1 </span>| <span class="varname"> item2 </span></span> </p> </td> 
  <td class="stentry"> <p>Uma barra vertical indica que o item de sintaxe único à esquerda ou o item à direita podem ser usados. Deve ser selecionado exatamente um item. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> { <span class="varname"> grupo </span>} </span> </p> </td> 
  <td class="stentry"> <p>As chaves são usadas para agrupar elementos de sintaxe. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> *{ <span class="varname"> grupo </span>} </span> </p> </td> 
  <td class="stentry"> <p>Os elementos de sintaxe dentro do grupo podem ser repetidos uma ou mais vezes. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>espaço em branco </p> </td> 
  <td class="stentry"> <p>Espaço em branco (espaços ou tabulações) não é permitido em solicitações HTTP. Este documento utiliza ocasionalmente espaços em branco entre elementos sintáticos apenas para maior clareza. </p> </td> 
 </tr> 
</table>

