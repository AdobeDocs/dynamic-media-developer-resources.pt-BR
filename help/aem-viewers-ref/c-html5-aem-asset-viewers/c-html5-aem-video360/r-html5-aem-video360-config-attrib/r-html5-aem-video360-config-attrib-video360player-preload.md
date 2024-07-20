---
title: Video360Player.preload
description: Indica se o visualizador começa a carregar o conteúdo de vídeo antes de a reprodução começar.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 33c28ed3-cdb3-4b14-8cc7-90f77ec9a3bb
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---

# Video360Player.preload{#video-player-preload}

Indica se o visualizador começa a carregar o conteúdo de vídeo antes de a reprodução começar.

`[Video360Player.|<containerId>_video360Player.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Se definido como <span class="codeph"> 1 </span>, o vídeo começa a ser baixado logo após a definição do ativo. Caso contrário, o pré-carregamento será iniciado somente após a reprodução ser iniciada pelo usuário final ou por uma chamada de API. </p> <p>Se definido como <span class="codeph"> 0 </span>, alguns recursos podem não funcionar até que a reprodução comece. Especificamente, a operação de busca não atualiza o quadro de vídeo. Se a imagem do pôster estiver desativada, o visualizador será exibido como uma área vazia em vez do primeiro quadro do vídeo. </p> <p>A desativação do pré-carregamento de vídeo pode ser ignorada em determinadas versões dos navegadores Internet Explorer 11 e Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
