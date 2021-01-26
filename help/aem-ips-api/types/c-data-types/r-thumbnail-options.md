---
description: Um tipo opcional que permite escolher um quadro de vídeo específico para usar como imagem em miniatura.
seo-description: Um tipo opcional que permite escolher um quadro de vídeo específico para usar como imagem em miniatura.
seo-title: OpçõesMiniaturas
solution: Experience Manager
title: OpçõesMiniaturas
topic: Dynamic Media Image Production System API
uuid: 50b2ecee-8396-4323-83e1-1f5060bec6c4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# ThumbnailOptions{#thumbnailoptions}

Um tipo opcional que permite escolher um quadro de vídeo específico para usar como imagem em miniatura.

Sintaxe

## Parâmetros {#section-b1777bf868764a7099d4a954b471856c}

<table id="table_C71FD0C995D94CE18994CDA2DC3460DF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbnailTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> <p>Define o tempo (em milissegundos a partir do start de vídeo) do quadro que você deseja usar para a miniatura do vídeo. Os valores variam de 0 ao final do vídeo. <p>Observação: O sistema usa o primeiro quadro do vídeo para a miniatura se você especificar a hora incorretamente. Consulte <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section-ce3b59c60fea4cd4945427a025051447}

```
<complexType name="ThumbnailOptions">
     <sequence>
        <element name="thumbnailTime" type="xsd:long" minOccurs="0"/>
      </sequence>
</complexType>
```

