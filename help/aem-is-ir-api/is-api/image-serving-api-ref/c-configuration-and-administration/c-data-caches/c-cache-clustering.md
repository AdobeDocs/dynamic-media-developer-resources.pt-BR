---
description: O agrupamento de cache permite que vários servidores com balanceamento de carga troquem entradas de cache no cache de resposta principal e no cache de dados secundário (para solicitações aninhadas/incorporadas), com o potencial de aumentar significativamente a capacidade de resposta do servidor, eliminando a necessidade de gerar a mesma entrada de cache em vários servidores.
solution: Experience Manager
title: Cluster de cache
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d1bea565-ac4e-4717-a53f-cbe706664598
TQID: 'https://experienceleague.adobe.com/J1QtNEy9i67oveb1oS2V6-fagqrrlC30oih8AS1g-N4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 305
ht-degree: 0%

---

# Cluster de cache{#cache-clustering}

O agrupamento de cache permite que vários servidores com balanceamento de carga troquem entradas de cache no cache de resposta principal e no cache de dados secundário (para solicitações aninhadas/incorporadas), com o potencial de aumentar significativamente a capacidade de resposta do servidor, eliminando a necessidade de gerar a mesma entrada de cache em vários servidores.

Se configurado dessa forma, quando um servidor recebe uma solicitação para um item que não está no cache local, ele contata os servidores pares no cluster. Ele verifica se eles já têm esse item de dados antes de solicitar que o Servidor de imagens gere o item.

O agrupamento de cache beneficia principalmente os aplicativos que envolvem conteúdo altamente armazenável em cache. As cargas do servidor devem ser significativamente reduzidas durante a implantação inicial e ao entrar em funcionamento com novos conteúdos.

Os tempos limite e outras proteções garantem que o sistema continue a funcionar com capacidade total mesmo quando um ou mais servidores de mesmo nível estiverem offline.

O cluster armazenado em cache pode operar em uma das duas configurações básicas:

* Quando `PS::cacheCluster.updateLocalCache` está habilitado (padrão), qualquer entrada de cache encontrada em um servidor par é copiada para o cache local.

  Essa configuração reduz o tráfego entre os servidores de mesmo nível. Ele também oferece os tempos de resposta mais rápidos, ao custo de ter todas as entradas de cache replicadas para todos os servidores do cluster. Essa é a configuração recomendada.

* Quando `PS::cacheCluster.updateLocalCache` está desabilitado, os dados de outros servidores não são copiados para o cache local.

  Isso multiplica o espaço em disco disponível para dados do cache. No entanto, aumenta o tráfego entre os servidores de peer e reduz os tempos de resposta geral. Use essa configuração somente quando você vir taxas de ocorrência de cache baixas.
