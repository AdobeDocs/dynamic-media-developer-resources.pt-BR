---
description: Siga estas instruções para desinstalar a Renderização de imagem em um sistema Linux ou Solaris.
solution: Experience Manager
title: Desinstalação no Linux e no Solaris
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# Desinstalação no Linux e no Solaris{#uninstalling-on-linux-and-solaris}

Siga estas instruções para desinstalar a Renderização de imagem em um sistema Linux ou Solaris.

Há duas maneiras de desinstalar a Renderização de imagem em um sistema Linux ou Solaris.

**Método 1**

1. Localizar [!DNL uninstall.sh].

   Está localizado no diretório do qual o ImageRendering foi instalado. Se este diretório tiver sido removido, o pacote de instalação original deverá ser descompactado e não poderá ser extraído [!DNL uninstall.sh].
1. Execute [!DNL uninstall.sh] e siga as instruções na tela.

>**Método 2**
>
>1. Parar a renderização de imagem com: ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
>1. Remova ImageRendering do seu sistema.

>
>   
O comando para remover ImageRendering depende do sistema:
>
>   Linux: `rpm -e ImageRendering`
>
>   Solaris: `pkgrm ImageRendering`
>
>1. Exclua todos os diretórios ou arquivos que não foram removidos na Etapa 2.

>


