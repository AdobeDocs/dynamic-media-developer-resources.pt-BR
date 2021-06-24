---
description: Indica se o visualizador começa a carregar conteúdo de vídeo antes do início da reprodução.
solution: Experience Manager
title: Video360Player.preload
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo 360 VR
role: Developer,Business Practitioner
exl-id: 33c28ed3-cdb3-4b14-8cc7-90f77ec9a3bb
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 4%

---

# Video360Player.preload{#video-player-preload}

Indica se o visualizador começa a carregar conteúdo de vídeo antes do início da reprodução.

`[Video360Player.|<containerId>_video360Player.]preload=0|1`

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
