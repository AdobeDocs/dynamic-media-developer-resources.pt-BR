---
title: cache
description: Controle de cache. Permite desabilitar seletivamente o cache do lado do cliente (navegador, servidores proxy, sistemas de cache de rede) e o cache no cache interno  [!DNL Platform Server] .
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b631836-e5a8-4a56-a09a-35bb2474cc84
TQID: 'https://experienceleague.adobe.com/-52nQ085AMsFuqDNv8JdEtXjwYFtIr3aXfHlrERSDoI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 260
ht-degree: 0%

---

# cache{#cache}

Controle de cache. Permite desabilitar seletivamente o cache do lado do cliente (navegador, servidores proxy, sistemas de cache de rede) e o cache no cache interno [!DNL Platform Server].

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> ativado|desativado|validar|atualizar</span> </p> </td> 
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

Se apenas um valor de `*`cacheControl`*` for especificado, ele será aplicado aos caches do cliente e do servidor.

A palavra-chave `validate` permite a atualização de entradas de cache após a alteração de arquivos de imagem, sem precisar aguardar a expiração automática da entrada de cache. O cache do cliente não é afetado por esse comando.

A palavra-chave `update` pode ser usada para forçar a atualização de entradas de cache do lado do servidor. Isso é útil depois que os recursos foram alterados e não são rastreados diretamente pelo mecanismo de validação de cache, como quando um arquivo de fonte é modificado sem alterar seu nome de arquivo ou a ID de fonte associada.

Se especificado em uma solicitação aninhada, `cache=on` habilita o cache persistente do lado do servidor da imagem gerada pela solicitação aninhada. Tenha cuidado para habilitar o armazenamento em cache de solicitações aninhadas somente quando houver a expectativa de que a mesma solicitação aninhada seja chamada repetidamente com exatamente os mesmos parâmetros.

## Propriedades {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

Solicitar atributo. Aplica-se independentemente da configuração atual da camada. Ignorado quando a solicitação não retorna uma imagem de resposta. *`clientControl`* é ignorado quando o cache do lado do cliente é desabilitado pelo catálogo de imagens (se `catalog::Expiration` tiver um valor negativo).

O controle de cache do lado do cliente (somente `on` e `off`) também está disponível para solicitações de conteúdo estático em [!DNL /is/content/].

## Padrão {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` para solicitações HTTP, `cache=off` para solicitações aninhadas/inseridas, `cache=on` para solicitações de conteúdo estático.

## Consulte também {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[catálogo::Expiração](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
