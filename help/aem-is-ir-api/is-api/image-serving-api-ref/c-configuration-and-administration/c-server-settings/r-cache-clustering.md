---
description: Use essas configurações de servidor para clustering de cache.
solution: Experience Manager
title: Cluster do cache
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# Cluster do cache{#cache-clustering}

Use essas configurações de servidor para clustering de cache.

## PS::cacheCluster.hosts - Hosts {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

Lista de endereços IP, separados por ponto e vírgula. Inclua os endereços IP de todos os servidores de mesmo nível a partir dos quais esse host deve obter dados de cache. O endereço IP do host local pode ser incluído para conveniência; isso permite as mesmas configurações para todos os servidores no cluster.

## PS::cacheCluster.updateLocalCache - Atualizar Cache Local {#section-154c2c0af4544200a3499232bb130dde}

Defina como &#39;Sim&#39; se uma entrada de cache fornecida por um servidor de mesmo nível deve ser copiada para o cache de resposta local.

## PS::cacheCluster.queryTimeout - Tempo limite da consulta {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

Ao solicitar uma entrada de cache de servidores de mesmo nível, o servidor aguardará até que um servidor responda que tem esse item de dados específico, ou até que todos os servidores de mesmo nível tenham respondido que não têm o item de dados ou até que o tempo especificado com essa configuração (em ms) tenha expirado.

## PS::cacheCluster.fetchTimeout - Tempo Limite de Busca {#section-41c42a29a26f43dc9cff50ad9fae1f14}

Especifica o número máximo de ms que o servidor aguardará para que os dados do cache real sejam entregues a partir do servidor peer. Se os dados completos não tiverem sido entregues antes do tempo limite expirar, o servidor presumirá que o peer está indisponível. A entrada do cache é então gerada localmente.
