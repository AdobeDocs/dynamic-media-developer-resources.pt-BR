---
description: Controle de cache. Permite desativar seletivamente o armazenamento em cache no lado do cliente (navegador, servidores proxy, sistemas de armazenamento em cache de rede) e o armazenamento em cache no cache interno do Servidor de Plataforma.
seo-description: Controle de cache. Permite desativar seletivamente o armazenamento em cache no lado do cliente (navegador, servidores proxy, sistemas de armazenamento em cache de rede) e o armazenamento em cache no cache interno do Servidor de Plataforma.
seo-title: cache
solution: Experience Manager
title: cache
uuid: 10332f0d-4ed3-4981-8034-46dffa5d68b0
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '131'
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
