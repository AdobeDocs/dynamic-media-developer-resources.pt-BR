---
description: Siga estas instruções para desinstalar a renderização de imagem em um sistema Linux ou Solaris.
seo-description: Siga estas instruções para desinstalar a renderização de imagem em um sistema Linux ou Solaris.
seo-title: Desinstalação no Linux e no Solaris
solution: Experience Manager
title: Desinstalação no Linux e no Solaris
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 80c0d6ec-985b-4596-bd67-22e5029f7b37
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# Desinstalação no Linux e no Solaris{#uninstalling-on-linux-and-solaris}

Siga estas instruções para desinstalar a renderização de imagem em um sistema Linux ou Solaris.

Há duas maneiras de desinstalar a renderização de imagem em um sistema Linux ou Solaris.

**Método 1**

1. Localizar [!DNL uninstall.sh].

   Está localizado no diretório a partir do qual ImageRendering foi instalado. Se esse diretório tiver sido removido, o pacote de instalação original deverá ser descompactado e não reiniciado para extrair [!DNL uninstall.sh].
1. Execute [!DNL uninstall.sh] e siga as instruções na tela.

>**Método 2**
>
>1. Parar renderização de imagem com: ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
>1. Remova ImageRendering do seu sistema.

>
>   
O comando para remover ImageRendering depende do seu sistema:
>
>   Linux: `rpm -e ImageRendering`
>
>   Solaris: `pkgrm ImageRendering`
>
>1. Exclua os diretórios ou arquivos que não foram removidos na Etapa 2.

>



