---
description: Antes de usar o Dynamic Media Image Serving, verifique se seu sistema atende aos requisitos do sistema.
solution: Experience Manager
title: Requisitos e pré-requisitos do sistema
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---


# Requisitos e pré-requisitos do sistema{#system-requirements-and-prerequisites}

Antes de usar o Dynamic Media Image Serving, verifique se seu sistema atende aos requisitos do sistema.

## Hardware do servidor {#section-f3c14a7bc1b745118602659628df779f}

O servidor deve atender aos seguintes requisitos de hardware.

>[!NOTE]
>
>Sistemas com processadores AMD64 e Intel® EM64T são configurados normalmente como plataformas NUMA (Non-Uniform Memory Architecture). Isso significa que o kernel constrói vários nós de memória no momento da inicialização em vez de construir um único nó de memória. A construção de vários nós pode resultar no esgotamento da memória em um ou mais nós, antes que outros nós fiquem esgotados. Quando ocorre esgotamento de memória, o kernel pode decidir interromper processos (por exemplo, o Servidor de Imagem ou o Servidor de Plataforma) mesmo que haja memória disponível. Portanto, a Adobe Systems recomenda que, se você estiver executando esse sistema, desative o NUMA. Use a opção `numa=off` start para evitar que o kernel pare esses processos.

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

**Observação (Linux):** o Serviço de imagem não funciona com o SELinux ativado. Essa opção é ativada por padrão. Para desativar o SELinux, edite o arquivo [!DNL /etc/selinux/config] e altere o valor do SELinux de:

`SELINUX=enforcing`

para

`SELINUX=disabled`

**Observação (Linux):** verifique se o nome do host do servidor pode ser resolvido para um endereço IP. Se isso não for possível, adicione o nome de host totalmente qualificado e o endereço IP a [!DNL /etc/hosts], como no exemplo a seguir.

`<ip address> <fully qualified hostname>`

## Software de servidor {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

O Dynamic Media Image Serving requer o seguinte software de servidor.

**Windows**

* Microsoft® Windows 2008 Server.
* Sistema operacional de 64 bits.

**Linux**

* Red Hat® Enterprise 5 ou CentOS 5.5 e posterior, com os patches de correção mais recentes.
* Sistema operacional de 64 bits.

**Observação:** para usar o Serviço de imagem no Windows, você deve instalar o Microsoft Visual Studio 2010 redistribuível. O redistribuível está disponível no seguinte local:

[http://www.microsoft.com/en-us/download/details.aspx?id=13523](http://www.microsoft.com/en-us/download/details.aspx?id=13523)

