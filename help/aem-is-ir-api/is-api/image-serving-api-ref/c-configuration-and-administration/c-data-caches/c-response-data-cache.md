---
description: O Platform Server armazena em cache todas as imagens de resposta e certos dados de texto em disco, a menos que uma solicitação seja marcada como não armazenável em cache.
seo-description: O Platform Server armazena em cache todas as imagens de resposta e determinados dados de texto em disco, a menos que uma solicitação seja marcada como não armazenável em cache.
seo-title: Cache de dados de resposta
solution: Experience Manager
title: Cache de dados de resposta
topic: Scene7 Image Serving - Image Rendering API
uuid: dbfda210-3b50-4e8c-8d77-7263ae4e80a2
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# Cache de dados de resposta{#response-data-cache}

O Platform Server armazena em cache todas as imagens de resposta e determinados dados de texto em disco, a menos que uma solicitação seja marcada como não armazenável em cache.

O local do cache de disco do Platform Server é definido com `PS::cache.rootPaths`.

Para aplicativos com altas taxas de ocorrência em cache, é possível aumentar o desempenho e a capacidade do servidor distribuindo o cache de dados de resposta entre vários dispositivos de disco. Isso é feito criando uma pasta raiz de cache em cada disco e registrando-os em `PS::cache.rootPaths`.

`PS::cache.maxSize` especifica o tamanho total de todas as entradas de cache, não considerando nenhuma sobrecarga do sistema de arquivos. A quantidade de espaço em disco realmente necessária depende das propriedades do sistema de arquivos, como o tamanho do bloco de disco e o número de entradas do cache. É recomendável reservar o dobro de espaço em disco para o cache de disco HTTP, da quantidade especificada por `PS::cache.maxSize`. Um algoritmo usado recentemente é empregado para manter a quantidade de dados em cache dentro do limite.

Além disso, `PS::cache.maxSize`o cache de resposta também é gerenciado pela limitação do número máximo de entradas do cache com `PS::cache.maxEntries`. No Linux, essa configuração deve especificar um valor não maior que o número de nós disponíveis na partição do cache.

>[!NOTE]
>
>O Platform Server mantém um índice de cache na memória. O tamanho desse índice é 32 bytes vezes o valor de `PS::cache.maxEntries`. Talvez seja necessário aumentar o tamanho do heap do Platform Server para acomodar caches maiores.

O sistema usa um arquivo de índice de cache salvo em disco quando o servidor é desligado de forma ordenada. Em caso de eventos inesperados, como falha de energia, esse arquivo pode não ser salvo. Além disso, pode levar vários minutos para o Platform Server ficar pronto.
