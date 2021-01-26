---
description: Script de controle do Servidor de imagens. Esse script é usado para start, parada ou reinicialização do Supervisor do Servidor de Servidor de Imagem, que, por sua vez, start, para ou reinicia todos os outros componentes do Servidor de Imagem.
seo-description: Script de controle do Servidor de imagens. Esse script é usado para start, parada ou reinicialização do Supervisor do Servidor de Servidor de Imagem, que, por sua vez, start, para ou reinicia todos os outros componentes do Servidor de Imagem.
seo-title: ImageServing
solution: Experience Manager
title: ImageServing
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 2975b957-e06f-42c6-8c0a-0d2757a0025a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 0%

---


# ImageServing{#imageserving}

Script de controle do Servidor de imagens. Esse script é usado para start, parada ou reinicialização do Supervisor do Servidor de Servidor de Imagem, que, por sua vez, start, para ou reinicia todos os outros componentes do Servidor de Imagem.

## Uso {#section-6832b5b10404442a9d3a3eca92041002}

` ImageServing *`comando`*`

## Comandos {#section-90436a0b0f70435f9ac42dafeed2c17b}

<table id="table_692C6A043F9747C88929FF20373EC88C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Comando </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> start  </span> </p> </td> 
   <td colname="col2"> <p> Start o Server Supervisor e todos os outros componentes do Serviço de imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stop  </span> </p> </td> 
   <td colname="col2"> <p> Pare todos os componentes do Servidor de imagens, incluindo o Supervisor de Servidor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reiniciar  </span> </p> </td> 
   <td colname="col2"> <p>Reinicie todos os componentes do Servidor de imagens, incluindo o Supervisor de Servidor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reiniciar { ps | is | svg }  </span> </p> </td> 
   <td colname="col2"> <p> Reinicie o servidor Tomcat/Platform, o servidor de imagens ou SVG. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> status [ ps | is | svg ]  </span> </p> </td> 
   <td colname="col2"> <p>Retorna informações de tempo de funcionamento e uso de memória atual para o Servidor de imagens, Tomcat/Platform Server e SVGserver, ou status apenas para o servidor especificado; uma mensagem informativa é retornada se o Supervisor de Servidor não estiver em execução. </p> </td> 
  </tr> 
 </tbody> 
</table>

