---
description: Script de controle do Servidor de imagem. Esse script é usado para iniciar, parar ou reiniciar o Supervisor do Servidor de Exibição de Imagens, que, por sua vez, inicia, interrompe ou reinicia todos os outros componentes do Servidor de Imagem.
solution: Experience Manager
title: ImageServing
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '156'
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
