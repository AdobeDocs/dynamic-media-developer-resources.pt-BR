---
description: Script de controle do Servidor de imagem. Esse script é usado para iniciar, parar ou reiniciar o Supervisor do Servidor de Exibição de Imagens, que, por sua vez, inicia, interrompe ou reinicia todos os outros componentes do Servidor de Imagem.
seo-description: Script de controle do Servidor de imagem. Esse script é usado para iniciar, parar ou reiniciar o Supervisor do Servidor de Exibição de Imagens, que, por sua vez, inicia, interrompe ou reinicia todos os outros componentes do Servidor de Imagem.
seo-title: ImageServing
solution: Experience Manager
title: ImageServing
uuid: 2975b957-e06f-42c6-8c0a-0d2757a0025a
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---


# ImageServing{#imageserving}

Script de controle do Servidor de imagem. Esse script é usado para iniciar, parar ou reiniciar o Supervisor do Servidor de Exibição de Imagens, que, por sua vez, inicia, interrompe ou reinicia todos os outros componentes do Servidor de Imagem.

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
   <td colname="col2"> <p> Inicie o Server Supervisor e todos os outros componentes do Image Serving. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> stop  </span> </p> </td> 
   <td colname="col2"> <p> Pare todos os componentes do Image Serving, incluindo o Supervisor de Servidor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reiniciar  </span> </p> </td> 
   <td colname="col2"> <p>Reinicie todos os componentes do Image Serving, incluindo o Server Supervisor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reiniciar { ps | é | svg }  </span> </p> </td> 
   <td colname="col2"> <p> Reinicializa o servidor Tomcat/Platform, o servidor de imagem ou o SVG. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> status [ ps | é | svg ]  </span> </p> </td> 
   <td colname="col2"> <p>Retorna informações de tempo de atividade e uso de memória atual para o Servidor de Imagem, Tomcat/Platform Server e SVGserver, ou status somente para o servidor especificado; uma mensagem informativa é retornada se o Supervisor de Servidor não estiver em execução. </p> </td> 
  </tr> 
 </tbody> 
</table>

