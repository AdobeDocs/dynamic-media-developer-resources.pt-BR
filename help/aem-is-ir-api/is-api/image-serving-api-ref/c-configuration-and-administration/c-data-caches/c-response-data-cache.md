---
description: O [!DNL Platform Server] armazena em cache todas as imagens de resposta e determinados dados de texto em disco, a menos que uma solicitação seja marcada como não armazenável em cache.
solution: Experience Manager
title: Cache de dados de resposta
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Cache de dados de resposta{#response-data-cache}

O [!DNL Platform Server] armazena em cache todas as imagens de resposta e determinados dados de texto em disco, a menos que uma solicitação seja marcada como não armazenável em cache.

A localização da variável [!DNL Platform Server]O cache de disco do está definido com `PS::cache.rootPaths`.

Para aplicativos com altas taxas de ocorrência de cache, você pode aumentar o desempenho e a capacidade do servidor distribuindo o cache de dados de resposta entre vários dispositivos de disco. Para isso, crie uma pasta raiz de cache em cada disco e registre-a em `PS::cache.rootPaths`.

`PS::cache.maxSize` especifica o tamanho total de todas as entradas de cache, não considerando nenhuma sobrecarga do sistema de arquivos. A quantidade de espaço em disco realmente necessária depende das propriedades do sistema de arquivos, como o tamanho do bloco de disco e o número de entradas de cache. É recomendável reservar duas vezes mais espaço em disco para o cache de disco HTTP que a quantidade especificada por `PS::cache.maxSize`. Um algoritmo usado menos recentemente é usado para manter a quantidade de dados em cache dentro do limite.

Além de `PS::cache.maxSize`, o cache de resposta também é gerenciado pela limitação do número máximo de entradas de cache com `PS::cache.maxEntries`. No Linux, essa configuração deve especificar um valor não maior que o número de nós disponíveis na partição do cache.

>[!NOTE]
>
>O [!DNL Platform Server] mantém um índice de cache na memória. O tamanho deste índice é 32 bytes vezes o valor de `PS::cache.maxEntries`. Pode ter necessidade de aumentar a [!DNL Platform Server] tamanho do heap para acomodar caches maiores.

O sistema usa um arquivo de índice de cache que é salvo em disco quando o servidor é desligado de forma ordenada. No caso de eventos inesperados, como falha de energia, esse arquivo pode não ser salvo. Além disso, pode levar vários minutos para a variável [!DNL Platform Server] para se preparar.
