---
title: UseLastModified
description: Habilitar cabeçalhos de resposta modificados por último. Ativa ou desativa a inclusão do cabeçalho Last-Modified em respostas HTTP armazenáveis em cache emitidas pela Renderização de imagem.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 31dfbc55-0efd-417b-be4a-67c878772388
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---

# UseLastModified{#uselastmodified}

Habilitar cabeçalhos de resposta modificados por último. Ativa ou desativa a inclusão do cabeçalho Last-Modified em respostas HTTP armazenáveis em cache emitidas pela Renderização de imagem.

O servidor usa o valor `vignette::TimeStamp` e `catalog::TimeStamp` mais recente de todos os registros de vinheta e catálogos/catálogos de material envolvidos em uma resposta como o valor do cabeçalho Última Modificação.

Deve ser habilitado somente se uma rede de cache distribuída, como a Akamai, for usada sem suporte para cabeçalhos etag.

>[!NOTE]
>
>Tenha cuidado ao usar cabeçalhos de Última modificação em um ambiente com balanceamento de carga envolvendo vários hosts de Servidor de imagens/Renderização. O armazenamento em cache do cliente pode ser derrotado e a carga do servidor aumentar se, por algum motivo, os servidores tiverem carimbos de data e hora diferentes para as mesmas entradas de catálogo. Essa situação pode ocorrer da seguinte forma:

* `catalog::TimeStamp`, `vignette::TimeStamp` ou `attribute::TimeStamp` não está definido, portanto, a hora de modificação do arquivo [!DNL catalog.ini] é usada como padrão para `catalog::TimeStamp`.

* Em vez de compartilhar os arquivos de catálogo de materiais por meio de uma montagem em rede, cada servidor tem sua própria instância dos arquivos de catálogo em um sistema de arquivos local.
* Duas ou mais instâncias do mesmo arquivo [!DNL catalog.ini] têm datas de modificação de arquivo diferentes, possivelmente causadas pela cópia incorreta dos arquivos.

## Propriedades {#section-453952244193452caccfaf7f601007c1}

Sinalizador. 0 para desativar, 1 para ativar cabeçalhos HTTP de Última Modificação.

## Padrão {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Herdado de `default::UseLastModified` se não estiver definido ou se estiver vazio.

## Consulte também {#section-1536715169da48b0aecc4ab7326c86db}

[catálogo::CarimboHora](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vinheta::CarimboHora](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
