---
title: VideoPlayer.preload
description: Indica se o visualizador começa a carregar o conteúdo de vídeo antes de a reprodução começar.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: cee887f6-bbd9-46dd-aa41-03493596fcf4
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---

# VideoPlayer.preload{#videoplayer-preload}

Indica se o visualizador começa a carregar o conteúdo de vídeo antes de a reprodução começar.

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Se definida como <span class="codeph"> 1 </span> o download do vídeo começa logo após a definição do ativo; caso contrário, o pré-carregamento começa somente após a reprodução ser iniciada pelo usuário final ou por uma chamada de API. </p> <p>Se definida como <span class="codeph"> 0 </span> alguns recursos podem não funcionar até que a reprodução comece; especificamente, a operação de busca não atualiza o quadro do vídeo. Se a imagem do pôster estiver desativada, o visualizador será exibido como uma área vazia em vez do primeiro quadro do vídeo. </p> <p>A desativação do pré-carregamento de vídeo pode ser ignorada em determinadas versões do Internet Explorer 11 e dos navegadores Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
