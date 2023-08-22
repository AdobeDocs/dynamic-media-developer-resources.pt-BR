---
title: cache
description: Controle de cache. Permite desabilitar seletivamente o cache do lado do cliente (navegador, servidores proxy, sistemas de cache de rede) e o cache na interface interna [!DNL Platform Server] cache.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b631836-e5a8-4a56-a09a-35bb2474cc84
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# cache{#cache}

Controle de cache. Permite desabilitar seletivamente o cache do lado do cliente (navegador, servidores proxy, sistemas de cache de rede) e o cache na interface interna [!DNL Platform Server] cache.

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> ativar|desativar|validar|atualizar</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> ligado|desligado</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> ligado|desligado</span> </p></td> 
 </tr> 
</table>

Se somente um `*`cacheControl`*` for especificado, será aplicado aos caches do cliente e do servidor.

A variável `validate` permite a atualização de entradas do cache após a alteração de arquivos de imagem, sem precisar aguardar a expiração automática da entrada do cache. O cache do cliente não é afetado por esse comando.

A variável `update` pode ser usada para forçar a atualização de entradas de cache do lado do servidor. Isso é útil depois que os recursos foram alterados e não são rastreados diretamente pelo mecanismo de validação de cache, como quando um arquivo de fonte é modificado sem alterar seu nome de arquivo ou a ID de fonte associada.

Se especificado em uma solicitação aninhada, `cache=on` permite o cache persistente do lado do servidor da imagem gerada pela solicitação aninhada. Tenha cuidado para habilitar o armazenamento em cache de solicitações aninhadas somente quando houver a expectativa de que a mesma solicitação aninhada seja chamada repetidamente com exatamente os mesmos parâmetros.

## Propriedades {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

Solicitar atributo. Aplica-se independentemente da configuração atual da camada. Ignorado quando a solicitação não retorna uma imagem de resposta. *`clientControl`*é ignorado quando o cache do lado do cliente é desativado pelo catálogo de imagens (se `catalog::Expiration` tem um valor negativo).

Controle de cache do lado do cliente ( `on` e `off` também está disponível para solicitações de conteúdo estático em [!DNL /is/content/].

## Padrão {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` para solicitações HTTP, `cache=off` para solicitações aninhadas/incorporadas, `cache=on` para solicitações de conteúdo estático.

## Consulte também {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[catálogo::Expiração](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
