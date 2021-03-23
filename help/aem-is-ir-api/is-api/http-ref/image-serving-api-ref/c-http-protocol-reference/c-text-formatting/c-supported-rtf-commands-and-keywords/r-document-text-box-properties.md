---
description: As seguintes propriedades de documento são suportadas em caixas de texto.
seo-description: As seguintes propriedades de documento são suportadas em caixas de texto.
seo-title: Propriedades do documento (caixa de texto)
solution: Experience Manager
title: Propriedades do documento (caixa de texto)
uuid: 743a773a-83b0-4667-9c67-4cefbfe77bbd
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '230'
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
   <td> <p>Extensão do Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl  </span> </td> 
   <td> <p>Tabela de cores para cores de exibição de imagens. </p> </td> 
   <td> <p>Extensão Dynamic Media; <span class="codeph"> apenas textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente de cor vermelha. </p> </td> 
   <td> <p>Pode aparecer somente em <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \verde  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente de cor verde. </p> </td> 
   <td> <p>Pode aparecer somente em <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \blue  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente de cor azul. </p> </td> 
   <td> <p>Pode aparecer somente em <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ciano  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente de cor ciano. </p> </td> 
   <td> <p>Extensão Dynamic Media; pode aparecer somente em <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente de cor magenta. </p> </td> 
   <td> <p>Extensão Dynamic Media; pode aparecer somente em <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \amarelo  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente de cor amarela. </p> </td> 
   <td> <p>Extensão Dynamic Media; pode aparecer somente em <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \black  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Componente de cor preta. </p> </td> 
   <td> <p>Extensão Dynamic Media; pode aparecer somente em <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margin  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Margem esquerda. </p> </td> 
   <td> <p>Twips; <span class="codeph"> apenas textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margr  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Margem direita. </p> </td> 
   <td> <p>Twips; <span class="codeph"> apenas textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margin  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Margem superior. </p> </td> 
   <td> <p>Twips; <span class="codeph"> apenas textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margin  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Margem inferior. </p> </td> 
   <td> <p>Twips; <span class="codeph"> apenas textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt  </span> </td> 
   <td> <p>Alinha o texto na caixa de texto. </p> </td> 
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
   <td> <p>Fluxo de texto específico da língua; <span class="codeph"> textPs= </span> somente 0 (padrão) esquerda-direita, parte superior-inferior (Europeu) 1 parte superior-inferior, direita-esquerda (Extremo leste) </p> </td> 
  </tr> 
 </tbody> 
</table>

