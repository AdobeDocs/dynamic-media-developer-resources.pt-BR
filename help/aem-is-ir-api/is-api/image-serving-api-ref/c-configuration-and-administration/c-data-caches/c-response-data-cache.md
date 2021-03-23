---
description: O Servidor da Plataforma armazena em cache todas as imagens de resposta e determinados dados de texto em disco, a menos que uma solicitação seja marcada como não armazenável em cache.
seo-description: O Servidor da Plataforma armazena em cache todas as imagens de resposta e determinados dados de texto em disco, a menos que uma solicitação seja marcada como não armazenável em cache.
seo-title: Cache de dados de resposta
solution: Experience Manager
title: Cache de dados de resposta
uuid: dbfda210-3b50-4e8c-8d77-7263ae4e80a2
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---


# Cache de dados de resposta{#response-data-cache}

O Servidor da Plataforma armazena em cache todas as imagens de resposta e determinados dados de texto em disco, a menos que uma solicitação seja marcada como não armazenável em cache.

O local do cache de disco do Servidor de Plataforma é definido com `PS::cache.rootPaths`.

Para aplicativos com altas taxas de ocorrência de cache, você pode aumentar o desempenho e a capacidade do servidor distribuindo o cache de dados de resposta entre vários dispositivos de disco. Para isso, crie uma pasta raiz de cache em cada disco e registre-a em `PS::cache.rootPaths`.

`PS::cache.maxSize` especifica o tamanho total de todas as entradas de cache, não considerando nenhuma sobrecarga do sistema de arquivos. A quantidade de espaço em disco realmente necessária depende das propriedades do sistema de arquivos, como o tamanho do bloco de disco e o número de entradas de cache. É recomendável reservar duas vezes mais espaço em disco para o cache de disco HTTP que a quantidade especificada por `PS::cache.maxSize`. Um algoritmo usado menos recentemente é usado para manter a quantidade de dados em cache dentro do limite.

Além de `PS::cache.maxSize`, o cache de resposta também é gerenciado limitando o número máximo de entradas de cache com `PS::cache.maxEntries`. No Linux, essa configuração deve especificar um valor não maior que o número de nós disponíveis na partição do cache.

>[!NOTE]
>
>O servidor da plataforma mantém um índice de cache na memória. O tamanho desse índice é 32 bytes vezes o valor de `PS::cache.maxEntries`. Talvez seja necessário aumentar o tamanho do heap do Platform Server para acomodar caches maiores.

O sistema usa um arquivo de índice de cache que é salvo em disco quando o servidor é desligado de forma ordenada. No caso de eventos inesperados, como falha de energia, esse arquivo pode não ser salvo. Além disso, pode levar vários minutos para que o Servidor da Plataforma fique pronto.
