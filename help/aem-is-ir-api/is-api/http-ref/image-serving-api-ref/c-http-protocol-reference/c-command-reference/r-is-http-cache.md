---
description: Controle de cache. Permite desativar seletivamente o armazenamento em cache no lado do cliente (navegador, servidores proxy, sistemas de armazenamento em cache de rede) e o armazenamento em cache no cache interno do Servidor de Plataforma.
seo-description: Controle de cache. Permite desativar seletivamente o armazenamento em cache no lado do cliente (navegador, servidores proxy, sistemas de armazenamento em cache de rede) e o armazenamento em cache no cache interno do Servidor de Plataforma.
seo-title: cache
solution: Experience Manager
title: cache
uuid: 08f4e4d0-0f7d-48fe-956c-284af97c902e
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---


# cache{#cache}

Controle de cache. Permite desativar seletivamente o armazenamento em cache no lado do cliente (navegador, servidores proxy, sistemas de armazenamento em cache de rede) e o armazenamento em cache no cache interno do Servidor de Plataforma.

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> em|desativado|validar|atualizar</span> </p> </td> 
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

Se apenas um valor `*`cacheControl`*` for especificado, ele será aplicado aos caches de cliente e de servidor.

A palavra-chave `validate` permite a atualização das entradas de cache após a alteração dos arquivos de imagem, sem precisar aguardar a expiração automática da entrada de cache. O armazenamento em cache do cliente não é afetado por este comando.

A palavra-chave `update` pode ser usada para forçar a atualização das entradas de cache do lado do servidor. Isso é útil após a alteração dos recursos, que não são rastreados diretamente pelo mecanismo de validação do cache, como quando um arquivo de fonte é modificado sem alterar o nome do arquivo ou a ID de fonte associada.

Se especificado em uma solicitação aninhada, `cache=on` habilita o armazenamento em cache persistente no lado do servidor da imagem gerada pela solicitação aninhada. Deve-se tomar cuidado para permitir o armazenamento em cache de solicitações aninhadas somente quando se espera que a mesma solicitação aninhada seja chamada repetidamente com exatamente os mesmos parâmetros.

## Propriedades {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

Atributo da solicitação. Aplica-se independentemente da configuração de camada atual. Ignorado quando a solicitação não retorna uma imagem de resposta. *`clientControl`*é ignorado quando o armazenamento em cache do lado do cliente é desativado pelo catálogo de imagem (se `catalog::Expiration` tiver um valor negativo).

O controle de cache do lado do cliente ( `on` e `off` somente) também está disponível para solicitações de conteúdo estático em [!DNL /is/content/].

## Padrão {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` para solicitações HTTP,  `cache=off` para solicitações aninhadas/incorporadas,  `cache=on` para solicitações de conteúdo estático.

## Consulte também {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[catálogo::Expiração](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
