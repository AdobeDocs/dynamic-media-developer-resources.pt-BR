---
title: Cache de dados de resposta
description: O  [!DNL Platform Server] armazena em cache todas as imagens de resposta e determinados dados de texto no disco, a menos que uma solicitação esteja marcada como não armazenável em cache.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
TQID: 'https://experienceleague.adobe.com/zxZqRHFCMKKDxOBb35IEZWEhTFhknDgCKcYatA6lqGs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 282
ht-degree: 0%

---

# Cache de dados de resposta{#response-data-cache}

O [!DNL Platform Server] armazena em cache todas as imagens de resposta e determinados dados de texto no disco, a menos que uma solicitação esteja marcada como não armazenável em cache.

O local do cache de disco de [!DNL Platform Server] está definido como `PS::cache.rootPaths`.

Para aplicativos com altas taxas de acerto de cache, você pode aumentar o desempenho e a capacidade do servidor distribuindo o cache de dados de resposta entre vários dispositivos de disco. Você consegue isso criando uma pasta raiz de cache em cada disco e registrando-os em `PS::cache.rootPaths`.

O `PS::cache.maxSize` especifica o tamanho total de todas as entradas do cache, sem considerar a sobrecarga do sistema de arquivos. A quantidade de espaço em disco necessária depende das propriedades do sistema de arquivos — como o tamanho do bloco do disco — e do número de entradas do cache. Reserve para o cache de disco HTTP o dobro do espaço em disco especificado por `PS::cache.maxSize`. Um algoritmo menos usado recentemente é empregado para manter a quantidade de dados em cache dentro do limite.

Além de `PS::cache.maxSize`, o cache de resposta também é gerenciado pela limitação do número máximo de entradas de cache com `PS::cache.maxEntries`. No Linux®, essa configuração deve especificar um valor não maior que o número de inodes disponíveis na partição do cache.

>[!NOTE]
>
>O [!DNL Platform Server] mantém um índice de cache na memória. O tamanho deste índice é de 32 bytes vezes o valor de `PS::cache.maxEntries`. Aumente o tamanho do heap [!DNL Platform Server] para acomodar caches maiores, se necessário.

O sistema usa um arquivo de índice de cache que é salvo em disco quando o servidor é desligado de forma ordenada. Se houver eventos inesperados, como falta de energia, esse arquivo pode não ser salvo. Além disso, pode levar vários minutos para que [!DNL Platform Server] fique pronto.
