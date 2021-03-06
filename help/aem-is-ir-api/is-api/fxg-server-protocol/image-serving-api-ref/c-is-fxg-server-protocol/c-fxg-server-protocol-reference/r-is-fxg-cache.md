---
description: Controle de cache. Permite desativar seletivamente o armazenamento em cache no lado do cliente (navegador, servidores proxy, sistemas de armazenamento em cache de rede) e o armazenamento em cache no cache interno do Servidor de Plataforma.
solution: Experience Manager
title: cache
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 622c36fa-c209-4149-a7db-85067215b5e5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---

# cache{#cache}

Controle de cache. Permite desativar seletivamente o armazenamento em cache no lado do cliente (navegador, servidores proxy, sistemas de armazenamento em cache de rede) e o armazenamento em cache no cache interno do Servidor de Plataforma.

`&cache= *`cacheControl`*`

`&cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> ativado|desativado</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> ativado|desativado</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> ativado|desativado</span> </p></td> 
 </tr> 
</table>

Se apenas um valor *`cacheControl`* for especificado, ele será aplicado aos caches do cliente e do servidor.

Atributo da solicitação. Ignorado quando a solicitação não retorna uma imagem de resposta. *`clientControl`* é ignorada quando o armazenamento em cache do lado do cliente é desativado pelo catálogo de imagem (se  `catalog::Expiration` tiver um valor negativo).

O padrão é `cache=on,on`.
