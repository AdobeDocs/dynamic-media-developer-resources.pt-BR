---
title: Arquivos de configuração do servidor
description: Todos os arquivos de configuração estão na install_folder/conf e são editáveis com a maioria dos editores de texto. Reinicie o servidor para que as alterações entrem em vigor.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6261844c-b63d-477b-8a48-963be868aa22
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# Arquivos de configuração do servidor{#server-configuration-files}

Todos os arquivos de configuração estão no `install_folder/conf` e são editáveis com a maioria dos editores de texto. Reinicie o servidor para que as alterações entrem em vigor.

>[!NOTE]
>
>A maioria dos arquivos de configuração do servidor contém propriedades e valores adicionais que não estão descritos neste documento. Essas propriedades são para uso interno do servidor e não devem ser modificadas, a menos que instruídas pelo suporte técnico da Dynamic Media.

Este documento discute as configurações dos seguintes arquivos de configuração:

<table id="table_D307B20E65B742A7AC3DEBF1E650719E"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Arquivo de configuração</b> </th> 
   <th class="entry"> <b>Descrição</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="filepath">SupervisorRegistry.xml</span> </p> </td> 
   <td> <p>Configuração do Supervisor do Servidor. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> server.xml</span> </p> </td> 
   <td> <p>Configuração do Tomcat. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath">PlatformServer.conf</span> </p> </td> 
   <td> <p>[!DNL Platform Server] configuração. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> catalog-service.conf</span> </p> </td> 
   <td> <p>Configuração do serviço de catálogo. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> monitor.conf</span> </p> </td> 
   <td> <p>Configuração de Monitoramento de Servidor. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="filepath"> ImageServerRegistry.xml</span> </p> </td> 
   <td> <p>Configuração do servidor de imagens. </p> </td> 
  </tr> 
 </tbody> 
</table>

Os arquivos de configuração são discutidos com mais detalhes posteriormente neste documento.
