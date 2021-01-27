---
description: Indica se o visualizador começa a carregar o conteúdo do vídeo antes dos start de reprodução.
seo-description: Indica se o visualizador começa a carregar o conteúdo do vídeo antes dos start de reprodução.
seo-title: Video360Player.preload
solution: Experience Manager
title: Video360Player.preload
topic: Dynamic Media
uuid: 6e3b95b8-d585-4164-8665-6211000689fe
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 5%

---


# Video360Player.preload{#video-player-preload}

Indica se o visualizador começa a carregar o conteúdo do vídeo antes dos start de reprodução.

`[Video360Player.|<containerId>_video360Player.]preload=0|1`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Se definido como <span class="codeph"> 1 </span> o vídeo começa a ser baixado logo após a definição do ativo; caso contrário, pré-carregue start somente depois que a reprodução for iniciada pelo usuário final ou por uma chamada de API. </p> <p>Se definido para <span class="codeph"> 0 </span> determinados recursos podem não funcionar até que os start de reprodução sejam reproduzidos; especificamente, a operação de busca não atualizará o quadro de vídeo. Se a imagem de pôster estiver desativada, o visualizador será exibido como uma área vazia em vez do primeiro quadro de vídeo. </p> <p>Observe que a desativação da pré-carga de vídeo pode ser ignorada em determinadas versões do Internet Explorer 11 e dos navegadores Edge. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preload=0`
