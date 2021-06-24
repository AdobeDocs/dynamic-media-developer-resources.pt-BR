---
description: Um tipo opcional que permite escolher um quadro de vídeo específico para usar como imagem em miniatura.
solution: Experience Manager
title: Opções de miniatura
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 7d84590d-2227-4d9a-9cb0-0f4b1fcabd8e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---

# Opções de miniatura{#thumbnailoptions}

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
   <td colname="col3"> <p>Define o tempo (em milissegundos a partir do início do vídeo) do quadro que deseja usar para a miniatura do vídeo. Os valores variam de 0 ao fim do vídeo. <p>Observação: O sistema usa o primeiro quadro do vídeo para a miniatura se você especificar o tempo incorretamente. Consulte <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p></p> </td> 
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
