---
description: Use essas configurações do servidor para configurar o servidor.
solution: Experience Manager
title: Servidor
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 10970ca8-b209-4adf-b027-6eb8d7a15db6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 0%

---

# Servidor{#server}

Use essas configurações do servidor para configurar o servidor.

## SV::ImageServerMode - modo de servidor de imagens {#section-991b287f2dde4f77a24fc69d5b32cabd}

As versões de 32 e 64 bits do Servidor de imagens estão disponíveis para Linux. Especifique ImageServer64 quando instalado em servidores Linux de 64 bits, ou ImageServer32 (padrão) quando instalado em servidores de 32 bits.

>[!NOTE]
>
>A versão de 64 bits do Servidor de imagens não suporta arquivos de origem FlashPix.

>[!NOTE]
>
>Não há suporte para o modo de 64 bits no Windows. Somente `ImageServer32` pode ser especificado. Caso contrário, o Servidor de imagens não será iniciado.

## SV::PsHeapSize - [!DNL Platform Server] Tamanho do Heap {#section-fd83715948764aeda58d6b3a9f9f8be9}

O tamanho do heap de Java para o [!DNL Platform Server]. O padrão é &quot; `512m`&quot; (512 Mbytes).

## IS::TcpPort, PS::isConnection.port - Porta de Escuta do Servidor de Imagens {#section-5421bfd2ca2a4a979faf812b6fdb2887}

Especifica a porta usada para comunicação entre o [!DNL Platform Server] e o Servidor de Imagens. Certifique-se de especificar um número de porta que não seja usado no sistema host.

>[!NOTE]
>
>Para que o Servidor de imagens funcione corretamente, o mesmo valor deve ser definido para `IS::TcpPort` e `PS::isConnection.port`.

## IS::PhysicalMemory - Limite de Memória do Servidor de Imagens {#section-85e37aa2ac6e456eb698da716dd3247d}

O limite aproximado de dados da imagem na memória, expresso como um percentual de memória física. O intervalo válido é de 10% a 90%. O Servidor de imagens tenta restringir seu uso de memória de imagem à quantidade especificada, se possível. O limite pode ser excedido temporariamente durante uma atividade intensa de processamento.

## IS::WorkerThreads - Número de Threads de Trabalho do Servidor de Imagens {#section-e2946063b13c4f728cdf5dba3d8b4de1}

O número máximo de threads que o Servidor de imagens usa para processar dados de imagem. O padrão é 0, o que permite que o Servidor de imagens otimize a contagem de threads automaticamente.

Alguns sistemas operacionais têm modelos de processos com uma alta sobrecarga de comutação de contexto. Em tal circunstância, o desempenho geral do servidor pode melhorar quando uma contagem de threads específica é selecionada (por exemplo, um thread por CPU). Algumas experiências podem ser necessárias para encontrar a configuração ideal. Consulte as notas de versão do Servidor de imagens e a documentação do sistema operacional para obter mais informações.

## IS::NumberOfTextServers - Número de Instâncias do Servidor de Texto {#section-971e20a90c1a473598fba738ed95671a}

O número máximo de renderizadores de texto que ficam ativos simultaneamente. 0 (padrão) é equivalente a 1,5 vez o número de núcleos do CPU disponíveis.

## IS::TextServerTcpPortRange - Portas de Comunicação do Servidor de Texto {#section-a13465de88ed4df09931e5ba840c1942}

As portas a serem usadas para comunicações do servidor de texto. Especifique a primeira e a última porta, separadas por &quot;-&quot;.
