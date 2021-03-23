---
description: Dados de taxa de bits múltipla.
seo-description: Dados de taxa de bits múltipla.
seo-title: mrSet
solution: Experience Manager
title: mrSet
uuid: 829c44ce-c66a-49a9-ba69-9e8e94ef8921
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---


# mrSet{#mbrset}

Dados de taxa de bits múltipla.

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

Retorna uma resposta de texto ou xml que contém uma lista de URLs (e as taxas de bits correspondentes) que correspondem às entradas de vídeo válidas no conjunto de vídeos associado à id de caminho de rede.

O requisito anterior de que uma entrada de vídeo válida contenha um valor para `catalog::VideoBitRate` foi relaxado. A entrada pode conter um valor para `catalog::VideoBitRate`*ou* `catalog::AudioBitRate`*ou* `catalog::TotalStreamBitRate`. Somente uma dessas opções precisa ser definida para que a entrada de vídeo seja válida. Observe que os requisitos para `catalog::Path` e uma extensão de arquivo de vídeo válida não foram alterados.

As respostas destinam-se ao consumo da Apple e dos servidores de transmissão de Flashes e, portanto, estão estruturalmente em conformidade com essas especificações. Os URLs são gerados usando prefixos `attribute::HttpAppleStreamingContext` e `attribute::HttpFlashStreamingContext`.

As respostas do m3u8 contêm apenas arquivos mp4, se houver algum presente no conjunto de vídeos. Se nenhum arquivo mp4 estiver presente, essas respostas conterão apenas arquivos f4v. Se nenhum arquivo mp4 ou f4v estiver presente, a resposta será vazia.

As respostas do f4m contêm arquivos f4v somente se houver algum no conjunto de vídeos. Se nenhum arquivo f4v estiver presente, essas respostas conterão apenas arquivos mp4. Se nenhum arquivo f4v ou arquivo mp4 estiver presente, a resposta será vazia.

As taxas de bits que aparecem nas respostas f4m/m3u8 correspondem aos valores em `catalog::TotalStreamBitRate` (convertidos em unidades apropriadas). Se `catalog::TotalStreamBitRate` não estiver definido, a soma de `catalog::VideoBitRate` e `catalog::AudioBitRate` é usada.

A resposta HTTP pode ser armazenada em cache com o TTL baseado em `catalog::NonImgExpiration`.
