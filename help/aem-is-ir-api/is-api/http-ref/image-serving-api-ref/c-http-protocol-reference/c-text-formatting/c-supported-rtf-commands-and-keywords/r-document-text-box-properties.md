---
description: As seguintes propriedades de documento são suportadas em caixas de texto.
seo-description: As seguintes propriedades de documento são suportadas em caixas de texto.
seo-title: Propriedades do documento (caixa de texto)
solution: Experience Manager
title: Propriedades do documento (caixa de texto)
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 743a773a-83b0-4667-9c67-4cefbfe77bbd
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---


# Propriedades do documento (caixa de texto){#document-text-box-properties}

As seguintes propriedades de documento são suportadas em caixas de texto.

<table id="table_8E1DF8E6BD894D7A9ACFC839918E2315"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Comando</b> </th> 
   <th class="entry"> <b>Descrição</b> </th> 
   <th class="entry"> <b>Notas</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \fonttbl  </span> </td> 
   <td> <p>Tabela de fontes. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Conjunto de caracteres para a fonte <i>N</i>. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colortbl  </span> </td> 
   <td> <p>Tabela de cores RGB. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolortbl  </span> </td> 
   <td> <p>Tabela de cores CMYK. </p> </td> 
   <td> <p>Extensão Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl  </span> </td> 
   <td> <p>Tabela de cores para cores do serviço de imagens. </p> </td> 
   <td> <p>extensão Dynamic Media; <span class="codeph"> textPs= </span> apenas </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente de cor vermelha. </p> </td> 
   <td> <p>Pode aparecer somente em <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \green  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente de cor verde. </p> </td> 
   <td> <p>Pode aparecer somente em <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blue  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente de cor azul. </p> </td> 
   <td> <p>Pode aparecer somente em <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cyan  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente de cor ciano. </p> </td> 
   <td> <p>extensão Dynamic Media; pode aparecer somente em <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente de cor magenta. </p> </td> 
   <td> <p>extensão Dynamic Media; pode aparecer somente em <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \amarelo  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente de cor amarela. </p> </td> 
   <td> <p>extensão Dynamic Media; pode aparecer somente em <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \black  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente de cor preta. </p> </td> 
   <td> <p>extensão Dynamic Media; pode aparecer somente em <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \marginal  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Margem esquerda. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> apenas </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margr  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Margem direita. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> apenas </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margt  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Margem superior. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> apenas </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Margem inferior. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> apenas </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt  </span> </td> 
   <td> <p>Alinha o texto acima na caixa de texto. </p> </td> 
   <td> <p>Padrão </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalb  </span> </td> 
   <td> <p>Alinha o texto na parte inferior da caixa de texto. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalc  </span> </td> 
   <td> <p>Centralizar texto na caixa de texto. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Orientação do fluxo de texto. </p> </td> 
   <td> <p>Fluxo de texto específico da língua; <span class="codeph"> textPs= </span> apenas 0 (padrão) esquerda-direita, superior-inferior (europeu) 1 cima-inferior, direita-esquerda (Far Oriental) </p> </td> 
  </tr> 
 </tbody> 
</table>

