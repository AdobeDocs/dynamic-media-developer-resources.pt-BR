---
description: O agrupamento de cache permite que vários servidores com balanceamento de carga troquem entradas de cache no cache de resposta principal e no cache de dados secundário (para solicitações aninhadas/incorporadas), com o potencial de aumentar significativamente a capacidade de resposta do servidor, eliminando a necessidade de gerar a mesma entrada de cache em vários servidores.
solution: Experience Manager
title: Cluster de cache
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d1bea565-ac4e-4717-a53f-cbe706664598
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '303'
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
