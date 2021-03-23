---
description: Habilite cabeçalhos de resposta da última modificação. Ativa ou desativa a inclusão do cabeçalho Last-Modified em respostas HTTP armazenáveis em cache emitidas pelo Serviço de imagem.
seo-description: Habilite cabeçalhos de resposta da última modificação. Ativa ou desativa a inclusão do cabeçalho Last-Modified em respostas HTTP armazenáveis em cache emitidas pelo Serviço de imagem.
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
uuid: 9dae4f15-4323-4f68-917f-6d72ae52c753
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---


# UseLastModified{#uselastmodified}

Habilite cabeçalhos de resposta da última modificação. Ativa ou desativa a inclusão do cabeçalho Last-Modified em respostas HTTP armazenáveis em cache emitidas pelo Serviço de imagem.

O servidor usa o valor `catalog::TimeStamp` mais recente de todos os catálogos/registros de catálogo envolvidos em uma resposta como o valor do cabeçalho Last-Modified .

Deve ser ativado somente se uma rede de armazenamento em cache distribuída ou outro sistema de armazenamento em cache for usado que não suporte cabeçalhos de tags.

>[!NOTE]
>
>Deve-se tomar cuidado ao usar cabeçalhos Last-Modified em um ambiente com balanceamento de carga envolvendo vários hosts do Image Serving. O armazenamento em cache do cliente pode ser derrotado e a carga do servidor aumentar se, por algum motivo, os servidores tiverem carimbos de data e hora diferentes para as mesmas entradas de catálogo. Tal situação pode ocorrer da seguinte forma:
>
>* `catalog::TimeStamp` nem `attribute::TimeStamp`, de modo que o tempo de modificação do arquivo [!DNL catalog.ini] seja usado como padrão para `catalog::TimeStamp`.
   >
   >
* Em vez de compartilhar os arquivos de catálogo de imagem por meio de uma montagem de rede, cada servidor tem sua própria instância dos arquivos de catálogo em um sistema de arquivos local.
>* Duas ou mais instâncias do mesmo arquivo [!DNL catalog.ini] têm datas de modificação de arquivo diferentes, possivelmente causadas pela cópia imprópria dos arquivos.

>



## Propriedades {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Sinalizador. 0 para desativar, 1 para ativar cabeçalhos HTTP Last-Modified.

## Padrão {#section-4eb47aadab8b41609bef296a4115f9f4}

Herdado de `default::UseLastModified` se não estiver definido ou se estiver vazio.

## Consulte também {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catálogo::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
