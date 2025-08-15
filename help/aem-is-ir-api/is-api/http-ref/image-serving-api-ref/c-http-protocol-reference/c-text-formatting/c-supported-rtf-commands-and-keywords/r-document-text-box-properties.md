---
description: As seguintes propriedades de documento são suportadas em caixas de texto.
solution: Experience Manager
title: Propriedades do documento (caixa de texto)
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e9d21a39-4d98-4115-8179-ab5acf713c80
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '225'
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
   <td> <span class="codeph"> \fonttbl </span> </td> 
   <td> <p>Tabela de fontes. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fcharset <span class="varname"> N </span> </span> </td> 
   <td> <p>Conjunto de caracteres para a fonte <i>N</i>. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \colortbl </span> </td> 
   <td> <p>Tabela de cores do RGB. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \cmykcolortbl </span> </td> 
   <td> <p>Tabela de cores CMYK. </p> </td> 
   <td> <p>Extensão do Dynamic Media. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \*\iscolortbl </span> </td> 
   <td> <p>Tabela de cores para cores do Servidor de imagens. </p> </td> 
   <td> <p>Extensão do Dynamic Media; <span class="codeph"> textPs= </span> somente </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \red <span class="varname"> N </span> </span> </td> 
   <td> <p>Componente de cor vermelha. </p> </td> 
   <td> <p>Pode aparecer apenas em <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \verde <span class="varname"> N </span> </span> </td> 
   <td> <p>Componente de cor verde. </p> </td> 
   <td> <p>Pode aparecer apenas em <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \azul <span class="varname"> N </span> </span> </td> 
   <td> <p>Componente de cor azul </p> </td> 
   <td> <p>Pode aparecer apenas em <span class="codeph"> \colortbl </span>; 0...255 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ciano <span class="varname"> N </span> </span> </td> 
   <td> <p>Componente de cor ciano. </p> </td> 
   <td> <p>A extensão do Dynamic Media; só pode aparecer em <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \magenta <span class="varname"> N </span> </span> </td> 
   <td> <p>Componente de cor magenta. </p> </td> 
   <td> <p>A extensão do Dynamic Media; só pode aparecer em <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \amarelo <span class="varname"> N </span> </span> </td> 
   <td> <p>Componente de cor amarela. </p> </td> 
   <td> <p>A extensão do Dynamic Media; só pode aparecer em <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \preto <span class="varname"> N </span> </span> </td> 
   <td> <p>Componente de cor preta. </p> </td> 
   <td> <p>A extensão do Dynamic Media; só pode aparecer em <span class="codeph"> \cmykcolortbl </span>; 0...100 </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margl <span class="varname"> N </span> </span> </td> 
   <td> <p>Margem esquerda. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> somente </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \marge <span class="varname"> N </span> </span> </td> 
   <td> <p>Margem direita. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> somente </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margt <span class="varname"> N </span> </span> </td> 
   <td> <p>Margem superior. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> somente </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \margb <span class="varname"> N </span> </span> </td> 
   <td> <p>Margem inferior. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> somente </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalt </span> </td> 
   <td> <p>Alinhar texto na parte superior da caixa de texto. </p> </td> 
   <td> <p>Padrão </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalb </span> </td> 
   <td> <p>Alinhar texto abaixo na caixa de texto. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \vertalc </span> </td> 
   <td> <p>Centralizar texto na caixa de texto. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \stextflow <span class="varname"> N </span> </span> </td> 
   <td> <p>Orientação do fluxo de texto. </p> </td> 
   <td> <p>Fluxo de texto específico do idioma; <span class="codeph"> textPs= </span> somente 0 (padrão) esquerda-direita, parte superior-inferior (europeu) 1 parte superior-inferior, direita-esquerda (Extremo Oriente) </p> </td> 
  </tr> 
 </tbody> 
</table>
