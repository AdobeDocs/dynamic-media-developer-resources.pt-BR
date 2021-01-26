---
description: Os servidores IS podem ser configurados para failover para servidores alternativos para solicitações que envolvam uma imagem de origem que não pode ser aberta ou lida com êxito.
seo-description: Os servidores IS podem ser configurados para failover para servidores alternativos para solicitações que envolvam uma imagem de origem que não pode ser aberta ou lida com êxito.
seo-title: Redirecionar para erro
solution: Experience Manager
title: Redirecionar para erro
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 894babe9-9c3c-4972-ae8f-387d65b4167d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---


# Redirecionar para erro{#redirect-on-error}

Os servidores IS podem ser configurados para failover para servidores alternativos para solicitações que envolvam uma imagem de origem que não pode ser aberta ou lida com êxito.

Os seguintes tipos de solicitações são redirecionados:

* IS Imagens que estão no catálogo, mas não no disco.

   Se uma imagem não estiver em um catálogo, o redirecionamento de erro não deverá ocorrer quando a imagem não puder ser encontrada.

* Imagens corrompidas, perfis coloridos ou fontes.
* O conteúdo estático não pode ser encontrado no disco.

   As solicitações de conteúdo estático são redirecionadas quando não podem ser encontradas no disco, mesmo se o conteúdo estático referenciado não tiver um registro de catálogo.

O redirecionamento de erros não ocorrerá em nenhum outro caso.

Quando ativado e esse erro ocorrer durante o processamento da solicitação, o servidor primário enviará a solicitação ao servidor secundário para processamento. A resposta, independentemente de indicar êxito ou falha, é encaminhada diretamente para o cliente. O servidor primário marca as entradas de log dessas solicitações encaminhadas com o uso do cache `REMOTE`. Os dados de resposta não são armazenados em cache localmente pelo servidor primário.

O redirecionamento de erro é ativado ao configurar `PS::errorRedirect.rootUrl` para o nome de domínio HTTP e o número da porta do servidor secundário. Além disso, o tempo limite da conexão é configurado com `PS::errorRedirect.connectTimeout` e o tempo máximo que o servidor primário aguardará uma resposta do servidor secundário antes de retornar um erro ao cliente é configurado com `PS::errorRedirect.socketTimeout`.

>[!NOTE]
>
>Se o servidor secundário não puder ser contatado, uma resposta de erro de texto será retornada ao cliente, mesmo se uma imagem padrão ou uma imagem de erro estiver configurada.

>[!NOTE]
>
>Caracteres de Pipe (|) no caminho de rede não são suportados para redirecionamento de erro.

## Consulte também {#section-2e8bfc128b944baf8108279d16492f3f}

[Redirecionamento de erro](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
