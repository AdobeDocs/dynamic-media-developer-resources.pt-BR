---
description: Ative os cabeçalhos de resposta da última modificação. Ativa ou desativa a inclusão do cabeçalho Última modificação em respostas HTTP passíveis de cache emitidas pela Renderização de imagem.
seo-description: Ative os cabeçalhos de resposta da última modificação. Ativa ou desativa a inclusão do cabeçalho Última modificação em respostas HTTP passíveis de cache emitidas pela Renderização de imagem.
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Scene7 Image Serving - Image Rendering API
uuid: f2ce2e04-4133-40af-ac82-cae57b253fe9
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---


# UseLastModified{#uselastmodified}

Ative os cabeçalhos de resposta da última modificação. Ativa ou desativa a inclusão do cabeçalho Última modificação em respostas HTTP passíveis de cache emitidas pela Renderização de imagem.

O servidor usa o mais recente `vignette::TimeStamp` e o `catalog::TimeStamp` valor de todos os catálogos/registros de catálogo de vinheta e material envolvidos em uma resposta como o valor do cabeçalho Última modificação.

Deve ser ativada somente se uma rede de armazenamento em cache distribuída, como Akamai, for usada e não suportar cabeçalhos de tag.

>[!NOTE]
>
>É necessário ter cuidado ao usar cabeçalhos Última modificação em um ambiente com balanceamento de carga que envolva vários hosts de disponibilização/renderização de imagem. O cache do cliente pode ser derrotado e a carga do servidor pode aumentar se, por algum motivo, os servidores tiverem carimbos de data e hora diferentes para as mesmas entradas do catálogo. Tal situação pode ocorrer do seguinte modo:

* Nem `catalog::TimeStamp`, `vignette::TimeStamp`, nem `attribute::TimeStamp` está definido, de modo que a hora de modificação do [!DNL catalog.ini] arquivo seja usada como padrão para `catalog::TimeStamp`.

* Em vez de compartilhar os arquivos de catálogo de materiais por meio de uma montagem de rede, cada servidor tem sua própria instância dos arquivos de catálogo em um sistema de arquivos local.
* Duas ou mais instâncias do mesmo [!DNL catalog.ini] arquivo têm datas de modificação de arquivo diferentes, possivelmente causadas pela cópia incorreta dos arquivos.

## Propriedades {#section-453952244193452caccfaf7f601007c1}

Sinalizar. 0 para desativar, 1 para ativar cabeçalhos HTTP modificados pela última vez.

## Padrão {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Herdado de `default::UseLastModified` se não estiver definido ou se estiver vazio.

## Consulte também {#section-1536715169da48b0aecc4ab7326c86db}

[catálogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vinheta::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
