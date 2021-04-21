---
description: Faça upload da configuração para processar arquivos ZIP e TAR como ativos primários (Nenhum) ou para extrair e carregar seu conteúdo (Uncompactar).
solution: Experience Manager
title: DescompactarOpções
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---


# DescompactarOpções{#uncompressoptions}

Faça upload da configuração para processar arquivos ZIP e TAR como ativos primários (Nenhum) ou para extrair e carregar seu conteúdo (Uncompactar).

>[!NOTE]
>
>`None` é padrão.

## Parâmetros {#section-10e49e27f60743da970a4ff1c4587eab}

<table id="table_89C2F7CDB24848459E47F1F7F58D91BA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> processo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Controla o processamento de arquivos ZIP e TAR. Fornece 2 opções: 
     <ul id="ul_F34E2F3B9B74450CA7E76BD9FD7137C2">
      <li id="li_E982468ED814446593B0C0A3F3D729FB"><span class="codeph"> Nenhum:</span> processar como ativos principais. </li>
      <li id="li_4A45DA99592B4EF7A1FE0A946A835104"><span class="codeph"> Descompactar:</span> extrair e processar conteúdo. </li>
     </ul><p>Observação: As constantes de cadeia de caracteres fazem distinção entre maiúsculas e minúsculas. Use <span class="codeph"> Descompacte</span>, não <span class="codeph"> descompacte</span> ou <span class="codeph"> descompacte</span>. </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section-48fd14af768a436284c31692038579a8}

```
 <!-- uncompress zip/tar/gzip files -->
            <element name="unCompressOptions" type="types:UnCompressOptions" minOccurs="0"/>
    <complexType name="UnCompressOptions">
        <sequence>
            <!-- Options: None (default),UnCompress -->
            <element name="process" type="xsd:string"/>
        </sequence>
    </complexType>
```

## Usado por {#section-b2a829cf5511412e968bb2000f85cc31}

O tipo `unCompressionOptions` é usado por:

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

