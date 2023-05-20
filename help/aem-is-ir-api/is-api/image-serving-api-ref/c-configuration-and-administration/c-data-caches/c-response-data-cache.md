---
description: A variável [!DNL Platform Server] armazena em cache toda a imagem de resposta e determinados dados de texto no disco, a menos que uma solicitação esteja marcada como não armazenável em cache.
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

A variável [!DNL Platform Server] armazena em cache toda a imagem de resposta e determinados dados de texto no disco, a menos que uma solicitação esteja marcada como não armazenável em cache.

A localização do [!DNL Platform Server]O cache de disco do está configurado com `PS::cache.rootPaths`.

Para aplicativos com altas taxas de acerto de cache, você pode aumentar o desempenho e a capacidade do servidor distribuindo o cache de dados de resposta entre vários dispositivos de disco. Você consegue isso criando uma pasta raiz de cache em cada disco e registrando-as em `PS::cache.rootPaths`.

`PS::cache.maxSize` especifica o tamanho total de todas as entradas do cache, sem considerar a sobrecarga do sistema de arquivos. A quantidade de espaço em disco realmente necessária depende das propriedades do sistema de arquivos — como o tamanho do bloco do disco — e do número de entradas do cache. É recomendável reservar o dobro de espaço em disco para o cache em disco HTTP do que a quantidade especificada por `PS::cache.maxSize`. Um algoritmo menos usado recentemente é empregado para manter a quantidade de dados em cache dentro do limite.

Além de `PS::cache.maxSize`, o cache de resposta também é gerenciado limitando o número máximo de entradas do cache com `PS::cache.maxEntries`. No Linux, essa configuração deve especificar um valor não maior que o número de inodes disponíveis na partição de cache.

>[!NOTE]
>
>A variável [!DNL Platform Server] O mantém um índice de cache na memória. O tamanho desse índice é de 32 bytes vezes o valor de `PS::cache.maxEntries`. Talvez seja necessário aumentar o [!DNL Platform Server] tamanho do heap para acomodar caches maiores.

O sistema usa um arquivo de índice de cache que é salvo em disco quando o servidor é desligado de forma ordenada. No caso de eventos inesperados, como falta de energia, esse arquivo pode não ser salvo. Além disso, pode levar vários minutos para que o [!DNL Platform Server] para ficar pronto.
