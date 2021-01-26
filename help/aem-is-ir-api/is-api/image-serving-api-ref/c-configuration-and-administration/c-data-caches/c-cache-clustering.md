---
description: O agrupamento em cache permite que vários servidores com balanceamento de carga troquem entradas de cache no cache de resposta principal e no cache de dados secundário (para solicitações aninhadas/incorporadas), com o potencial de aumentar significativamente a capacidade de resposta do servidor, eliminando a necessidade de gerar a mesma entrada de cache em vários servidores.
seo-description: O agrupamento em cache permite que vários servidores com balanceamento de carga troquem entradas de cache no cache de resposta principal e no cache de dados secundário (para solicitações aninhadas/incorporadas), com o potencial de aumentar significativamente a capacidade de resposta do servidor, eliminando a necessidade de gerar a mesma entrada de cache em vários servidores.
seo-title: Cluster de cache
solution: Experience Manager
title: Cluster de cache
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 347165d6-a9e7-406e-81a8-8a91f745ce27
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 0%

---


# Clustering de cache{#cache-clustering}

O agrupamento em cache permite que vários servidores com balanceamento de carga troquem entradas de cache no cache de resposta principal e no cache de dados secundário (para solicitações aninhadas/incorporadas), com o potencial de aumentar significativamente a capacidade de resposta do servidor, eliminando a necessidade de gerar a mesma entrada de cache em vários servidores.

Se configurado dessa forma, quando um servidor recebe uma solicitação de um item que não está no cache local, ele entra em contato com os servidores de mesmo nível no cluster. Verifica se eles já têm esse item de dados antes de solicitar ao Servidor de imagens que gere o item.

O agrupamento em cache beneficia principalmente os aplicativos que envolvem conteúdo altamente armazenável em cache. As cargas do servidor devem ser significativamente reduzidas durante a implantação inicial e ao entrar em operação com novos conteúdos.

Os tempos limite e outras salvaguardas garantem que o sistema continue a funcionar com capacidade total mesmo quando um ou mais dos servidores de mesmo nível estiverem offline.

O cluster de cache pode operar em uma das duas configurações básicas:

* Quando `PS::cacheCluster.updateLocalCache` estiver ativado (padrão), qualquer entrada de cache encontrada em um servidor de mesmo nível será copiada para o cache local.

   Essa configuração reduz o tráfego entre os servidores de mesmo nível. Ele também fornece os tempos de resposta mais rápidos, ao custo de ter todas as entradas de cache replicadas para todos os servidores no cluster. Esta é a configuração recomendada.

* Quando `PS::cacheCluster.updateLocalCache` estiver desativado, os dados de outros servidores não são copiados para o cache local.

   Isso multiplica o espaço em disco disponível para dados de cache. No entanto, ele aumenta o tráfego entre os servidores de mesmo nível e reduz o tempo geral de resposta. Use essa configuração somente quando você observar taxas baixas de ocorrência em cache.

