---
description: O clustering de cache permite que vários servidores com balanceamento de carga troquem entradas de cache no cache de resposta principal e no cache de dados secundário (para solicitações aninhadas/incorporadas), com o potencial para aumentar significativamente a capacidade de resposta do servidor, eliminando a necessidade de gerar a mesma entrada de cache em vários servidores.
solution: Experience Manager
title: Cluster do cache
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---


# Cluster do cache{#cache-clustering}

O clustering de cache permite que vários servidores com balanceamento de carga troquem entradas de cache no cache de resposta principal e no cache de dados secundário (para solicitações aninhadas/incorporadas), com o potencial para aumentar significativamente a capacidade de resposta do servidor, eliminando a necessidade de gerar a mesma entrada de cache em vários servidores.

Se configurado, quando um servidor recebe uma solicitação de um item que não está no cache local, ele entra em contato com os servidores de mesmo nível no cluster. Ele verifica se já tem esse item de dados antes de solicitar ao Servidor de imagem que gere o item.

O armazenamento em cluster de cache beneficia principalmente os aplicativos que envolvem conteúdo altamente armazenável em cache. As cargas do servidor devem ser significativamente reduzidas durante a implantação inicial e ao entrar em operação com novos conteúdos.

Os tempos limite e outras salvaguardas garantem que o sistema continue a funcionar com toda a capacidade, mesmo quando um ou mais dos servidores de mesmo nível estiverem offline.

O cluster de cache pode operar em uma das duas configurações básicas:

* Quando `PS::cacheCluster.updateLocalCache` está ativado (padrão), qualquer entrada de cache encontrada em um servidor de mesmo nível é copiada para o cache local.

   Essa configuração reduz o tráfego entre os servidores de mesmo nível. Ele também fornece os tempos de resposta mais rápidos a custo de ter todas as entradas de cache replicadas para todos os servidores no cluster. Essa é a configuração recomendada.

* Quando `PS::cacheCluster.updateLocalCache` está desativado, os dados de outros servidores não são copiados para o cache local.

   Isso multiplica o espaço em disco disponível para dados de cache. No entanto, aumenta o tráfego entre os servidores de mesmo nível e reduz os tempos de resposta gerais. Use essa configuração somente quando vir taxas de ocorrência de cache baixas.

