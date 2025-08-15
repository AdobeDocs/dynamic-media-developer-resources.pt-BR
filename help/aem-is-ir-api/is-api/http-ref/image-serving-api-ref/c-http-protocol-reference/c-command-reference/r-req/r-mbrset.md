---
description: Dados de taxa de múltiplos bits.
solution: Experience Manager
title: mbrSet
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0568a4a1-7d6a-453e-83bc-05c0cde0c0f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# mbrSet{#mbrset}

Dados de taxa de múltiplos bits.

`req=mbrSet[,text|xml[, *`codificação`*]][&fmt= *`fmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> codificação</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m | m3u8</span> </p></td> 
 </tr> 
</table>

Retorna uma resposta text ou xml que contém uma lista de URLs (e taxas de bits correspondentes) que correspondem a entradas de vídeo válidas no conjunto de vídeos associado à id do caminho de rede.

O requisito anterior, de que uma entrada de vídeo válida contenha um valor para `catalog::VideoBitRate`, foi relaxado. A entrada pode conter um valor para `catalog::VideoBitRate`*ou* `catalog::AudioBitRate`*ou* `catalog::TotalStreamBitRate`. Somente um deles precisa ser definido para que a entrada de vídeo seja válida. Observe que os requisitos para `catalog::Path` e uma extensão de arquivo de vídeo válida não foram alterados.

As respostas são destinadas ao consumo por Apple e Flash Streaming Servers e, portanto, estão estruturalmente em conformidade com essas especificações. As URLs são geradas usando os prefixos `attribute::HttpAppleStreamingContext` e `attribute::HttpFlashStreamingContext`.

as respostas m3u8 contêm apenas arquivos mp4, se houver algum presente no conjunto de vídeos. Se nenhum arquivo mp4 estiver presente, essas respostas conterão apenas arquivos f4v. Se não houver arquivos mp4 ou f4v, a resposta estará vazia.

As respostas do f4m contêm apenas arquivos f4v se houver algum no conjunto de vídeos. Se nenhum arquivo f4v estiver presente, essas respostas conterão apenas arquivos mp4. Se nenhum arquivo f4v ou mp4 estiver presente, a resposta estará vazia.

As taxas de bits que aparecem nas respostas f4m/m3u8 correspondem aos valores em `catalog::TotalStreamBitRate` (convertidos em unidades apropriadas). Se `catalog::TotalStreamBitRate` não estiver definido, a soma de `catalog::VideoBitRate` e `catalog::AudioBitRate` será usada.

A resposta HTTP pode ser armazenada em cache com o TTL com base em `catalog::NonImgExpiration`.
