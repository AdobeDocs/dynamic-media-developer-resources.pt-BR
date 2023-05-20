---
description: Os servidores IS podem ser configurados para failover para servidores alternativos para solicitações que envolvam uma imagem de origem que não possa ser aberta ou lida com êxito.
solution: Experience Manager
title: Redirecionar em caso de erro
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c5541bf3-3296-4ce3-a2ff-9f6336f78ea9
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 0%

---

# Redirecionar em caso de erro{#redirect-on-error}

Os servidores IS podem ser configurados para failover para servidores alternativos para solicitações que envolvam uma imagem de origem que não possa ser aberta ou lida com êxito.

Os seguintes tipos de solicitações são redirecionados:

* IS Imagens que estão no catálogo, mas não no disco.

   Se uma imagem não estiver em um catálogo, o redirecionamento de erro não deverá ocorrer quando a imagem não puder ser encontrada.

* Imagens, perfis de cores ou fontes corrompidos.
* O conteúdo estático não pode ser encontrado no disco.

   As solicitações de conteúdo estático são redirecionadas quando não podem ser encontradas no disco, mesmo que o conteúdo estático referenciado não tenha um registro de catálogo.

O redirecionamento de erro não ocorrerá em nenhum outro caso.

Quando habilitado e quando esse erro ocorrer durante o processamento da solicitação, o servidor primário enviará a solicitação ao servidor secundário para processamento. A resposta, independentemente de indicar sucesso ou falha, é encaminhada diretamente ao cliente. O servidor primário marca as entradas de log dessas solicitações encaminhadas com uso de cache `REMOTE`. Os dados de resposta não são armazenados em cache localmente pelo servidor primário.

O redirecionamento de erro está habilitado pela configuração `PS::errorRedirect.rootUrl` ao nome de domínio HTTP e ao número da porta do servidor secundário. Além disso, o tempo limite da conexão é configurado com o `PS::errorRedirect.connectTimeout` e o tempo máximo que o servidor primário aguardará uma resposta do servidor secundário antes de retornar um erro para o cliente que está configurado com o `PS::errorRedirect.socketTimeout`.

>[!NOTE]
>
>Se não for possível entrar em contato com o servidor secundário, uma resposta de erro de texto será retornada ao cliente, mesmo se uma imagem padrão ou de erro estiver configurada.

>[!NOTE]
>
>Caracteres de barra vertical (|) no caminho de rede não são suportados para redirecionamento de erro.

## Consulte também {#section-2e8bfc128b944baf8108279d16492f3f}

[Redirecionamento de erro](../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-error-redirection.md#reference-268b1bf6ce1b44bb979727c6f5daf1ac)
