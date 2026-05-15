---
description: Use essas configurações do servidor para clustering de cache.
solution: Experience Manager
title: Cluster de cache
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: bd0267e7-ebf5-4995-b55e-89cb1a58de6d
TQID: 'https://experienceleague.adobe.com/4SJmK1ILgnCBqYjjQcEnz0SVRzQfsY9mD05Xpd1ssnw'
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
source-wordcount: 200
ht-degree: 0%

---

# Cluster de cache{#cache-clustering}

Use essas configurações do servidor para clustering de cache.

## PS::cacheCluster.hosts - Hosts {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

Lista de endereços IP, separados por ponto e vírgula. Inclua os endereços IP de todos os servidores de mesmo nível dos quais este host deve obter dados de cache. O endereço IP do host local pode ser incluído para conveniência; isso permite as mesmas definições de configuração para todos os servidores no cluster.

## PS::cacheCluster.updateLocalCache - Atualizar cache local {#section-154c2c0af4544200a3499232bb130dde}

Defina como &#39;Sim&#39; se uma entrada de cache fornecida por um servidor de mesmo nível deve ser copiada para o cache de resposta local.

## PS::cacheCluster.queryTimeout - Tempo limite da consulta {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

Ao solicitar uma entrada de cache de servidores de mesmo nível, o servidor aguarda até que um servidor responda que tem esse item de dados específico, ou até que todos os servidores de mesmo nível respondam que não têm o item de dados, ou até que o tempo especificado com essa configuração (em ms) tenha expirado.

## PS::cacheCluster.fetchTimeout - Tempo limite de busca {#section-41c42a29a26f43dc9cff50ad9fae1f14}

Especifica o número máximo de milissegundos que o servidor aguarda até que os dados reais do cache sejam entregues pelo servidor par. Se os dados completos não tiverem sido entregues antes da expiração do tempo limite, o servidor presume que o peer se tornou indisponível. A entrada do cache é gerada localmente.
