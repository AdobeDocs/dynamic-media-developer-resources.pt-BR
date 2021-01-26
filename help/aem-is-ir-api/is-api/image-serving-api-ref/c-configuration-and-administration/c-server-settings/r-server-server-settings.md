---
description: Use essas configurações do servidor para configurar seu servidor.
seo-description: Use essas configurações do servidor para configurar seu servidor.
seo-title: Servidor
solution: Experience Manager
title: Servidor
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 50db98cc-8354-4884-9416-00808828061b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---


# Servidor{#server}

Use essas configurações do servidor para configurar seu servidor.

## SV::ImageServerMode - Modo do Servidor de Imagens {#section-991b287f2dde4f77a24fc69d5b32cabd}

Uma versão de 32 e 64 bits do Image Server está disponível para Linux. Especifique ImageServer64 quando instalado em servidores Linux de 64 bits, ou ImageServer32 (padrão) quando instalado em servidores de 32 bits.

>[!NOTE]
>
>A versão de 64 bits do Servidor de imagens não suporta arquivos de origem FlashPix.

>[!NOTE]
>
>O modo de 64 bits não é suportado no Windows. Somente `ImageServer32` pode ser especificado. Caso contrário, o Serviço de imagem não será start.

## SV::PsHeapSize - Tamanho do Heap do Servidor de Plataforma {#section-fd83715948764aeda58d6b3a9f9f8be9}

O tamanho do heap do Java para o Servidor da plataforma. O padrão é &quot; `512m`&quot; (512 Mbytes).

## IS::TcpPort, PS::isConnection.port - Porta de escuta do servidor de imagens {#section-5421bfd2ca2a4a979faf812b6fdb2887}

Especifica a porta usada para comunicação entre o Servidor de plataforma e o Servidor de imagem. Especifique um número de porta que não seja usado de outra forma no sistema host.

>[!NOTE]
>
>Para que o serviço de imagem funcione corretamente, o mesmo valor deve ser definido para `IS::TcpPort` e `PS::isConnection.port`.

## IS::PhysicalMemory - Image Server Memory Limit {#section-85e37aa2ac6e456eb698da716dd3247d}

O limite aproximado para dados de imagem na memória, expresso como uma porcentagem da memória física. O intervalo válido é de 10% a 90%. O Servidor de imagens tenta restringir seu uso de memória de imagem à quantidade especificada, se possível. O limite pode ser excedido temporariamente durante a atividade de processamento pesado.

## IS::WorkerThreads - Número de Threads de Trabalho do Image Server {#section-e2946063b13c4f728cdf5dba3d8b4de1}

O número máximo de threads que o Servidor de imagens usa para processar dados de imagem. O padrão é 0, o que permite que o Servidor de imagens otimize a contagem de threads automaticamente.

Alguns sistemas operacionais têm modelos de processos com uma sobrecarga de switching de contexto alta. Nesse caso, o desempenho geral do servidor pode melhorar quando uma contagem de threads específica é selecionada (por exemplo, um thread por CPU). Alguns testes podem ser necessários para encontrar a configuração ideal. Consulte as notas de versão do Servidor de imagens e a documentação do sistema operacional para obter mais informações.

## IS::NumberOfTextServers - Número de Instâncias do Servidor de Texto {#section-971e20a90c1a473598fba738ed95671a}

O número máximo de renderizadores de texto a serem ativos simultaneamente. 0 (padrão) equivale a 1,5 vezes o número de núcleos de CPU disponíveis.

## IS::TextServerTcpPortRange - Portas de Comunicação do Servidor de Texto {#section-a13465de88ed4df09931e5ba840c1942}

As portas a serem usadas para comunicações com o servidor de texto. Especifique o primeiro e o último número da porta, separados por &#39;-&#39;.
