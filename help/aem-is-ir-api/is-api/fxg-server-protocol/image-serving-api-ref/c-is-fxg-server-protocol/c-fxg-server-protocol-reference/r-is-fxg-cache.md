---
description: Controle de cache. Permite desativar seletivamente o cache do lado do cliente (navegador, servidores proxy, sistemas de cache de rede) e o cache no cache interno do Servidor de plataforma.
seo-description: Controle de cache. Permite desativar seletivamente o cache do lado do cliente (navegador, servidores proxy, sistemas de cache de rede) e o cache no cache interno do Servidor de plataforma.
seo-title: cache
solution: Experience Manager
title: cache
topic: Scene7 Image Serving - Image Rendering API
uuid: 10332f0d-4ed3-4981-8034-46dffa5d68b0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# cache{#cache}

Controle de cache. Permite desativar seletivamente o cache do lado do cliente (navegador, servidores proxy, sistemas de cache de rede) e o cache no cache interno do Servidor de plataforma.

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

Atributo de solicitação. Ignorado quando a solicitação não retorna uma imagem de resposta. *`clientControl`* é ignorada quando o cache do lado do cliente é desativado pelo catálogo de imagens (se  `catalog::Expiration` tiver um valor negativo).

O padrão é `cache=on,on`.
