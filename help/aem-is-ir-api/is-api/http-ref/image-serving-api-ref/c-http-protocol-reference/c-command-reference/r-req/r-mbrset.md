---
description: Dados de taxa de múltiplos bits.
solution: Experience Manager
title: mbrSet
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0568a4a1-7d6a-453e-83bc-05c0cde0c0f8
TQID: 'https://experienceleague.adobe.com/j8HXFZEv-TJINp20XNewqo82k-Yy39Aey4FU4Tm8AVc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 253
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
