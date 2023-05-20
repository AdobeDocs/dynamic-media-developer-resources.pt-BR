---
description: Habilitar cabeçalhos de resposta modificados por último. Ativa ou desativa a inclusão do cabeçalho Última modificação em respostas HTTP armazenáveis em cache emitidas pelo Servidor de imagens.
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# UseLastModified{#uselastmodified}

Habilitar cabeçalhos de resposta modificados por último. Ativa ou desativa a inclusão do cabeçalho Última modificação em respostas HTTP armazenáveis em cache emitidas pelo Servidor de imagens.

O servidor usa o mais recente `catalog::TimeStamp` valor de todos os catálogos/registros de catálogo envolvidos em uma resposta como o valor do cabeçalho Última modificação.

Deve ser habilitado somente se uma rede de cache distribuída ou outro sistema de cache for usado e não tiver suporte para cabeçalhos etag.

>[!NOTE]
>
>Tenha cuidado ao usar cabeçalhos de Última modificação em um ambiente com balanceamento de carga envolvendo vários hosts do Servidor de imagens. O armazenamento em cache do cliente pode ser derrotado e a carga do servidor aumentar se, por algum motivo, os servidores tiverem carimbos de data e hora diferentes para as mesmas entradas de catálogo. Essa situação pode ocorrer da seguinte forma:
>
>* Nenhuma `catalog::TimeStamp` nem `attribute::TimeStamp`, de modo a que o momento da modificação do [!DNL catalog.ini] O arquivo é usado como padrão para `catalog::TimeStamp`.
>
>* Em vez de compartilhar os arquivos do catálogo de imagens por meio de uma montagem de rede, cada servidor tem sua própria instância dos arquivos do catálogo em um sistema de arquivos local.
>* Duas ou mais instâncias do mesmo [!DNL catalog.ini] Os arquivos têm datas de modificação diferentes, possivelmente causadas pela cópia incorreta dos arquivos.
>


## Propriedades {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Sinalizador. 0 para desativar, 1 para ativar cabeçalhos HTTP de Última Modificação.

## Padrão {#section-4eb47aadab8b41609bef296a4115f9f4}

Herdado de `default::UseLastModified` se não estiver definido ou se estiver vazio.

## Consulte também {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catálogo::Carimbo de data/hora](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
