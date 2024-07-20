---
title: VideoPlayer.preload
description: Indica se o visualizador começa a carregar o conteúdo de vídeo antes de a reprodução começar.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: afabbfde-e003-4fee-a4ef-0fc4c43fd960
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---

# VideoPlayer.preload{#videoplayer-preload}

Indica se o visualizador começa a carregar o conteúdo de vídeo antes de a reprodução começar.

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Se definido como <span class="codeph"> 1 </span>, o download do vídeo começará logo após a definição do ativo; caso contrário, o pré-carregamento só será iniciado depois que a reprodução for iniciada pelo usuário final ou por uma chamada de API. </p> <p>Se definido como <span class="codeph"> 0 </span>, certos recursos podem não funcionar até que a reprodução comece; especificamente, a operação de busca não atualiza o quadro do vídeo. Se a imagem do pôster estiver desativada, o visualizador será exibido como uma área vazia em vez do primeiro quadro do vídeo. </p> <p>A desativação do pré-carregamento de vídeo pode ser ignorada em determinadas versões dos navegadores Internet Explorer 11 e Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
