---
description: Dados de taxa de vários bits.
seo-description: Dados de taxa de vários bits.
seo-title: mbrSet
solution: Experience Manager
title: mbrSet
topic: Scene7 Image Serving - Image Rendering API
uuid: 829c44ce-c66a-49a9-ba69-9e8e94ef8921
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# mbrSet{#mbrset}

Dados de taxa de vários bits.

`req=mbrSet[,text|xml[, *``*]][&fmt= *`encodingfmtType`*]`

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

Retorna uma resposta de texto ou xml que contém uma lista de URLs (e as taxas de bits correspondentes) que correspondem a entradas de vídeo válidas no conjunto de vídeos associado à id de caminho de rede.

O requisito anterior de que uma entrada de vídeo válida contenha um valor para `catalog::VideoBitRate` foi agora relaxado. A entrada pode conter um valor para `catalog::VideoBitRate`*ou* `catalog::AudioBitRate`*ou* `catalog::TotalStreamBitRate`. Apenas um deles precisa ser definido para que a entrada de vídeo seja válida. Observe que os requisitos para `catalog::Path` e uma extensão de arquivo de vídeo válida não foram alterados.

As respostas são destinadas ao consumo da Apple e dos Servidores de transmissão contínua de Flashes e, portanto, estão em conformidade estrutural com essas especificações. Os URLs são gerados usando prefixos `attribute::HttpAppleStreamingContext` e `attribute::HttpFlashStreamingContext`.

As respostas m3u8 só contêm arquivos mp4 se houver algum presente no conjunto de vídeos. Se nenhum arquivo mp4 estiver presente, essas respostas conterão apenas arquivos f4v. Se não houver arquivos mp4 nem arquivos f4v, a resposta estará vazia.

As respostas f4m só contêm arquivos f4v se houver algum presente no conjunto de vídeos. Se nenhum arquivo f4v estiver presente, essas respostas conterão apenas arquivos mp4. Se nenhum arquivo f4v ou mp4 estiver presente, a resposta estará vazia.

As taxas de bits que aparecem nas respostas f4m/m3u8 correspondem aos valores em `catalog::TotalStreamBitRate` (convertidos em unidades apropriadas). Se `catalog::TotalStreamBitRate` não estiver definido, a soma de `catalog::VideoBitRate` e `catalog::AudioBitRate` será usada.

A resposta HTTP pode ser armazenada em cache com o TTL baseado em `catalog::NonImgExpiration`.
