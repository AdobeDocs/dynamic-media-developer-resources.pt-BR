---
description: Um tipo opcional que permite escolher um quadro de vídeo específico para usar como imagem em miniatura.
seo-description: Um tipo opcional que permite escolher um quadro de vídeo específico para usar como imagem em miniatura.
seo-title: Opções de miniatura
solution: Experience Manager
title: Opções de miniatura
uuid: 50b2ecee-8396-4323-83e1-1f5060bec6c4
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '120'
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

