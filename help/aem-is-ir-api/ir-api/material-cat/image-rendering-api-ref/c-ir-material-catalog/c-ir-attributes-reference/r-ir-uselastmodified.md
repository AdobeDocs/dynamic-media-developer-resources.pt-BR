---
description: Habilite cabeçalhos de resposta da última modificação. Ativa ou desativa a inclusão do cabeçalho Last-Modified em respostas HTTP armazenáveis em cache emitidas pela Renderização de Imagem.
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---


# UseLastModified{#uselastmodified}

Habilite cabeçalhos de resposta da última modificação. Ativa ou desativa a inclusão do cabeçalho Last-Modified em respostas HTTP armazenáveis em cache emitidas pela Renderização de Imagem.

O servidor usa o valor mais recente `vignette::TimeStamp` e `catalog::TimeStamp` de todos os catálogos/registros de vinheta e material envolvidos em uma resposta como o valor de cabeçalho Última modificação .

Deve ser ativado somente se uma rede de armazenamento em cache distribuída, como o Akamai, for usada e não oferecer suporte a cabeçalhos de tags.

>[!NOTE]
>
>Deve-se tomar cuidado ao usar cabeçalhos Last-Modified em um ambiente com balanceamento de carga envolvendo vários hosts de Exibição/Renderização de imagem. O armazenamento em cache do cliente pode ser derrotado e a carga do servidor aumentar se, por algum motivo, os servidores tiverem carimbos de data e hora diferentes para as mesmas entradas de catálogo. Tal situação pode ocorrer da seguinte forma:

* `catalog::TimeStamp`, `vignette::TimeStamp`, ou `attribute::TimeStamp` não estão definidas, portanto, a hora de modificação do arquivo [!DNL catalog.ini] é usada como padrão para `catalog::TimeStamp`.

* Em vez de compartilhar os arquivos de catálogo de material por meio de uma montagem de rede, cada servidor tem sua própria instância dos arquivos de catálogo em um sistema de arquivos local.
* Duas ou mais instâncias do mesmo arquivo [!DNL catalog.ini] têm datas de modificação de arquivo diferentes, possivelmente causadas pela cópia imprópria dos arquivos.

## Propriedades {#section-453952244193452caccfaf7f601007c1}

Sinalizador. 0 para desativar, 1 para ativar cabeçalhos HTTP Last-Modified.

## Padrão {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Herdado de `default::UseLastModified` se não estiver definido ou se estiver vazio.

## Consulte também {#section-1536715169da48b0aecc4ab7326c86db}

[catálogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ,  [vinheta::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
