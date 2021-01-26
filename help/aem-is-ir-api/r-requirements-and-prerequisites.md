---
description: Antes de usar o Dynamic Media Image Server, verifique se o sistema atende aos requisitos do sistema.
seo-description: Antes de usar o Dynamic Media Image Server, verifique se o sistema atende aos requisitos do sistema.
seo-title: Requisitos e pré-requisitos do sistema
solution: Experience Manager
title: Requisitos e pré-requisitos do sistema
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 80196574-f5a2-4298-880a-cc36f90b6e21
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---


# Requisitos e pré-requisitos do sistema{#system-requirements-and-prerequisites}

Antes de usar o Dynamic Media Image Server, verifique se o sistema atende aos requisitos do sistema.

## Hardware do servidor {#section-f3c14a7bc1b745118602659628df779f}

Seu servidor deve atender aos seguintes requisitos de hardware.

>[!NOTE]
>
>Os sistemas com processadores AMD64 e Intel® EM64T geralmente são configurados como plataformas NUMA (Non-Uniform Memory Architecture). Isso significa que o kernel constrói vários nós de memória em tempo de inicialização, em vez de construir um único nó de memória. A construção de vários nós pode resultar em exaustão de memória em um ou mais nós antes que outros nós fiquem esgotados. Quando ocorre o esgotamento da memória, o kernel pode decidir matar processos (por exemplo, o Servidor de imagens ou o Servidor de plataformas) mesmo que haja memória disponível. Portanto, a Adobe Systems recomenda que, se você estiver executando um sistema desse tipo, desligue o NUMA. Use a opção de start `numa=off` para evitar que o kernel pare esses processos.

**Windows**

* CPU Intel Xeon® ou AMD® Opteron com pelo menos 4 núcleos.
* Mínimo de 16 GB de RAM.
* Troque o espaço pelo menos o dobro da quantidade de memória física (RAM).
* 2 GB de espaço em disco rígido disponível para instalação e operação básica, é necessário espaço em disco adicional para imagens de origem, registros, caches de dados e arquivos manifest.
* Placa de interface de rede Fast Ethernet.

**Linux**

* CPU Intel Xeon® ou AMD® Opteron com pelo menos 4 núcleos.
* Mínimo de 16 GB de RAM.
* Troca desativada (recomendado).
* 2 GB de espaço em disco rígido disponível para instalação e operação básica, é necessário espaço em disco adicional para imagens de origem, registros, caches de dados e arquivos manifest.
* Placa de interface de rede Fast Ethernet.

**Observação (Linux): o Serviço** de imagem não funciona com o SELinux ativado. Essa opção é ativada por padrão. Para desativar o SELinux, edite o arquivo [!DNL /etc/selinux/config] e altere o valor do SELinux de:

`SELINUX=enforcing`

to

`SELINUX=disabled`

**Observação (Linux):** certifique-se de que o nome do host do servidor possa ser resolvido para um endereço IP. Se isso não for possível, adicione o nome do host totalmente qualificado e o endereço IP a [!DNL /etc/hosts], como no exemplo a seguir.

`<ip address> <fully qualified hostname>`

## Software de servidor {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

O Dynamic Media Image Server requer o seguinte software de servidor.

**Windows**

* Microsoft® Windows 2008 Server.
* Sistema operacional de 64 bits.

**Linux**

* Red Hat® Enterprise 5 ou CentOS 5.5 e posterior, com as correções mais recentes.
* Sistema operacional de 64 bits.

**Observação:** para usar o Serviço de imagem no Windows, você deve instalar o Microsoft Visual Studio 2010 redistribuível. O redistribuível está disponível no seguinte local:

[http://www.microsoft.com/en-us/download/details.aspx?id=13523](http://www.microsoft.com/en-us/download/details.aspx?id=13523)

