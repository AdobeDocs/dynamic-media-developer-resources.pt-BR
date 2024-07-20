---
description: Script de controle do Servidor de imagens. Esse script é usado para iniciar, interromper ou reiniciar o Supervisor do Servidor de Servidor de Imagens, que, por sua vez, inicia, interrompe ou reinicia todos os outros componentes do Servidor de Imagens.
solution: Experience Manager
title: ImageServing
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 252e12d9-703e-4fbb-a156-8dcdc3bc4f2e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# ImageServing{#imageserving}

Script de controle do Servidor de imagens. Esse script é usado para iniciar, interromper ou reiniciar o Supervisor do Servidor de Servidor de Imagens, que, por sua vez, inicia, interrompe ou reinicia todos os outros componentes do Servidor de Imagens.

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
   <td colname="col1"> <p> <span class="codeph"> início </span> </p> </td> 
   <td colname="col2"> <p> Inicie o Supervisor de Servidor e todos os outros componentes do Servidor de Imagens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parada </span> </p> </td> 
   <td colname="col2"> <p> Pare todos os componentes do Servidor de imagens, incluindo o Supervisor de servidores. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reiniciar </span> </p> </td> 
   <td colname="col2"> <p>Reinicie todos os componentes do Servidor de imagens, incluindo o Supervisor de servidor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> reiniciar o { ps | é | svg } </span> </p> </td> 
   <td colname="col2"> <p> Reinicia o Tomcat/[!DNL Platform Server], o Servidor de imagens ou o SVG. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> status [ ps | é | svg ] </span> </p> </td> 
   <td colname="col2"> <p>Retorna informações de tempo de atividade e uso de memória atual para o Servidor de imagens, Tomcat/[!DNL Platform Server] e SVGserver, ou status apenas para o servidor especificado; uma mensagem informativa é retornada se o Supervisor de servidor não estiver em execução. </p> </td> 
  </tr> 
 </tbody> 
</table>
