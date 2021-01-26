---
description: Ative os cabeçalhos de resposta da última modificação. Ativa ou desativa a inclusão do cabeçalho Última modificação em respostas HTTP passíveis de cache emitidas pelo Serviço de imagem.
seo-description: Ative os cabeçalhos de resposta da última modificação. Ativa ou desativa a inclusão do cabeçalho Última modificação em respostas HTTP passíveis de cache emitidas pelo Serviço de imagem.
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9dae4f15-4323-4f68-917f-6d72ae52c753
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---


# UseLastModified{#uselastmodified}

Ative os cabeçalhos de resposta da última modificação. Ativa ou desativa a inclusão do cabeçalho Última modificação em respostas HTTP passíveis de cache emitidas pelo Serviço de imagem.

O servidor usa o valor `catalog::TimeStamp` mais recente de todos os catálogos/registros de catálogo envolvidos em uma resposta como o valor do cabeçalho Última modificação.

Deve ser ativado somente se uma rede de cache distribuída ou outro sistema de cache for usado que não suporte cabeçalhos de tag.

>[!NOTE]
>
>Deve-se ter cuidado ao usar cabeçalhos Última modificação em um ambiente com balanceamento de carga que envolva vários hosts do Servidor de imagens. O cache do cliente pode ser derrotado e a carga do servidor pode aumentar se, por algum motivo, os servidores tiverem carimbos de data e hora diferentes para as mesmas entradas do catálogo. Tal situação pode ocorrer do seguinte modo:
>
>* Nem `catalog::TimeStamp` nem `attribute::TimeStamp`, de modo que a hora de modificação do arquivo [!DNL catalog.ini] seja usada como padrão para `catalog::TimeStamp`.
   >
   >
* Em vez de compartilhar os arquivos de catálogo de imagens por meio de uma montagem de rede, cada servidor tem sua própria instância dos arquivos de catálogo em um sistema de arquivos local.
>* Duas ou mais instâncias do mesmo arquivo [!DNL catalog.ini] têm datas de modificação de arquivo diferentes, possivelmente causadas pela cópia incorreta dos arquivos.

>



## Propriedades {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Sinalizar. 0 para desativar, 1 para ativar cabeçalhos HTTP modificados pela última vez.

## Padrão {#section-4eb47aadab8b41609bef296a4115f9f4}

Herdado de `default::UseLastModified` se não estiver definido ou se estiver vazio.

## Consulte também {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catálogo::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
