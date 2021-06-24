---
description: Indica se o visualizador começa a carregar conteúdo de vídeo antes do início da reprodução.
solution: Experience Manager
title: VideoPlayer.preload
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Developer,Business Practitioner
exl-id: cee887f6-bbd9-46dd-aa41-03493596fcf4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 1%

---

# VideoPlayer.preload{#videoplayer-preload}

Indica se o visualizador começa a carregar conteúdo de vídeo antes do início da reprodução.

`[VideoPlayer.|<containerId>_videoPlayer.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Se definido como <span class="codeph"> 1 </span> o vídeo começa a ser baixado logo após a definição do ativo; caso contrário, o pré-carregamento só será iniciado depois que a reprodução for iniciada pelo usuário final ou por uma chamada de API. </p> <p>Se definido como <span class="codeph"> 0 </span> certos recursos podem não funcionar até que a reprodução seja iniciada; especificamente, a operação de busca não atualizará o quadro de vídeo. Se a imagem de pôster estiver desativada, o visualizador será exibido como uma área vazia em vez do primeiro quadro de vídeo. </p> <p>Observe que a desativação do pré-carregamento de vídeo pode ser ignorada em determinadas versões do Internet Explorer 11 e dos navegadores Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
