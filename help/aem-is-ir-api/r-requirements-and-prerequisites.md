---
description: Antes de usar o Dynamic Media Image Serving, verifique se seu sistema atende aos requisitos do sistema.
solution: Experience Manager
title: Requisitos e pré-requisitos do sistema
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# Requisitos e pré-requisitos do sistema{#system-requirements-and-prerequisites}

Antes de usar o Dynamic Media Image Serving, verifique se seu sistema atende aos requisitos do sistema.

## Hardware de servidor {#section-f3c14a7bc1b745118602659628df779f}

O servidor deve atender aos seguintes requisitos de hardware.

>[!NOTE]
>
>Sistemas com processadores AMD64 e Intel® EM64T são configurados normalmente como plataformas NUMA (Non-Uniform Memory Architecture). Isso significa que o kernel constrói vários nós de memória no momento da inicialização em vez de construir um único nó de memória. A construção de vários nós pode resultar no esgotamento da memória em um ou mais nós, antes que outros nós fiquem esgotados. Quando ocorre esgotamento de memória, o kernel pode decidir interromper processos (por exemplo, o Servidor de imagem ou [!DNL Platform Server]) mesmo que haja memória disponível. Portanto, a Adobe Systems recomenda que, se você estiver executando esse sistema, desative o NUMA. Use o `numa=off` opção start para evitar que o kernel interrompa esses processos.

**Windows**

* CPU Intel Xeon® ou AMD® Opteron com pelo menos 4 núcleos.
* Mínimo de 16 GB de RAM.
* Troque o espaço igual a pelo menos o dobro da quantidade de memória física (RAM).
* 2 GB de espaço em disco rígido disponível para instalação e operação básica, é necessário espaço em disco adicional para imagens de origem, registros, caches de dados e arquivos de manifesto.
* Placa de interface de rede Fast Ethernet.

**Linux**

* CPU Intel Xeon® ou AMD® Opteron com pelo menos 4 núcleos.
* Mínimo de 16 GB de RAM.
* Troca desabilitada (recomendada).
* 2 GB de espaço em disco rígido disponível para instalação e operação básica, é necessário espaço em disco adicional para imagens de origem, registros, caches de dados e arquivos de manifesto.
* Placa de interface de rede Fast Ethernet.

**Observação (Linux):** O Serviço de imagem não funciona com o SELinux ativado. Essa opção é ativada por padrão. Para desativar o SELinux, edite o [!DNL /etc/selinux/config] e altere o valor do SELinux de:

`SELINUX=enforcing`

para

`SELINUX=disabled`

**Observação (Linux):** Certifique-se de que o nome do host do servidor possa ser resolvido para um endereço IP. Se isso não for possível, adicione o nome de host totalmente qualificado e o endereço IP a [!DNL /etc/hosts] como no exemplo a seguir.

`<ip address> <fully qualified hostname>`

## Software de servidor {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

O Dynamic Media Image Serving requer o seguinte software de servidor.

**Windows**

* Servidor Microsoft® Windows 2008.
* Sistema operacional de 64 bits.

**Linux**

* Red Hat® Enterprise 5 ou CentOS 5.5 e posterior, com os patches de correção mais recentes.
* Sistema operacional de 64 bits.

**Observação:** Para usar o Serviço de Imagens no Windows, você deve instalar o Microsoft Visual Studio 2010 redistribuível.
