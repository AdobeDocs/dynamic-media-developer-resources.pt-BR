---
title: Requisitos e pré-requisitos do sistema
description: Antes de usar o Dynamic Media Image Serving, verifique se seu sistema atende aos requisitos do sistema.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
TQID: 'https://experienceleague.adobe.com/SKAe9OsVsSkTRR5E3s5lBcPct4CgG1h1uIh7ayIpINA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 390
ht-degree: 0%

---

# Requisitos e pré-requisitos do sistema{#system-requirements-and-prerequisites}

Antes de usar o Dynamic Media Image Serving, verifique se seu sistema atende aos requisitos do sistema.

## Hardware do servidor {#section-f3c14a7bc1b745118602659628df779f}

O servidor deve atender aos seguintes requisitos de hardware.

>[!NOTE]
>
>Os sistemas com processadores AMD64 e Intel® EM64T são normalmente configurados como plataformas NUMA (Non-Uniform Memory Architecture). Isso significa que o kernel constrói vários nós de memória no momento da inicialização em vez de construir um único nó de memória. A construção de vários nós pode resultar no esgotamento da memória em um ou mais nós antes que outros nós se esgotem. Quando ocorre esgotamento de memória, o kernel pode decidir eliminar processos (por exemplo, o Servidor de imagens ou [!DNL Platform Server]) mesmo que haja memória disponível. Portanto, a Adobe recomenda que, se você estiver executando esse sistema, desative o NUMA. Use a opção de início `numa=off` para evitar que o kernel interrompa esses processos.

**Janelas**

* CPU Intel Xeon® ou AMD® Opteron com pelo menos quatro núcleos.
* 1 GB de RAM, no mínimo.
* O espaço de troca é igual a pelo menos o dobro da quantidade de memória física (RAM).
* 2 GB de espaço disponível em disco rígido para instalação e operação básica, é necessário espaço adicional em disco para imagens de origem, registros, caches de dados e arquivos manifest.
* Placa de interface de rede Fast Ethernet.

**Linux®**

* CPU Intel Xeon® ou AMD® Opteron com pelo menos quatro núcleos.
* 16 GB de RAM, no mínimo.
* Troca desativada (recomendado).
* 2 GB de espaço disponível em disco rígido para instalação e operação básica, é necessário espaço adicional em disco para imagens de origem, registros, caches de dados e arquivos manifest.
* Placa de interface de rede Fast Ethernet.

**Observação (Linux®):** o Servidor de imagens não funciona com o SELinux ativado. Essa opção está ativada por padrão. Para desabilitar o SELinux, edite o arquivo [!DNL /etc/selinux/config] e altere o valor de SELinux de:

`SELINUX=enforcing`

Para

`SELINUX=disabled`

**Observação (Linux®):** verifique se o nome de host do servidor pode ser resolvido para um endereço IP. Se isso não for possível, adicione o nome de host totalmente qualificado e o endereço IP a [!DNL /etc/hosts], como no exemplo a seguir.

`<ip address> <fully qualified hostname>`

## Software de servidor {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

O Dynamic Media Image Serving exige o seguinte software de servidor.

**Janelas**

* Microsoft® Windows Server 2008
* Sistema operacional de 64 bits.

**Linux®**

* Red Hat® Enterprise 5 ou CentOS 5.5 e posteriores, com os patches de correção mais recentes.
* Sistema operacional de 64 bits.

**Observação:** para usar o Servidor de imagens no Windows, você deve instalar o Microsoft® Visual Studio 2010.
