---
description: Gera a imagem em miniatura do vídeo.
seo-description: Gera a imagem em miniatura do vídeo.
seo-title: MediaOptions
solution: Experience Manager
title: MediaOptions
uuid: 4de59678-1bef-484c-9a43-ded531537aeb
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# MediaOptions{#mediaoptions}

Gera a imagem em miniatura do vídeo.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoEncodingPresetsArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:HandleArray</span> </td> 
   <td colname="col3">Uma matriz de <span class="codeph"> PropertySet</span> lida com as predefinições de codificação de vídeo para transcodificação de vídeos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generateThumbnail</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Quando verdadeiro, o primeiro quadro do vídeo é extraído e usado como a imagem em miniatura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbnailOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:Opções de miniatura</span> </td> 
   <td colname="col3">Opcional. Permite que você escolha um quadro de vídeo específico para usar como imagem em miniatura. <p>Para especificar uma imagem em miniatura, passe o tempo (em milissegundos a partir do início do vídeo) do quadro que deseja usar. Os valores variam de 0 ao fim do vídeo. <p>Observação: Se você especificar a hora incorretamente, o padrão <span class="codeph"> generateThumbnail</span> será true. </p></p><p>Consulte <a href="../../types/c-data-types/r-thumbnail-options.md#reference-370088b0a4ce4096b9b3e5489a368b5c" format="dita" scope="local"> ThumbnailOptions</a>. </p></td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section-a9356de782d74af6933c39fa7ad12212}

```
<complexType name="MediaOptions">
        <sequence>
            <element name="videoEncodingPresetsArray" type="types:HandleArray" minOccurs="0"/>
            <element name="generateThumbnail" type="xsd:boolean" minOccurs="0"/>
            <element name="thumbnailOptions" type="types:ThumbnailOptions" minOccurs="0"/>
        </sequence>
    </complexType>
```

## Usado por {#section-87cb83407198432c95eaa2db9f12f9db}

O tipo `mediaOptions` é usado por:

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadURLsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

