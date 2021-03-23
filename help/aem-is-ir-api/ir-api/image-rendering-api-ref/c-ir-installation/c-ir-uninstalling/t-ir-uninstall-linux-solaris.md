---
description: Siga estas instruções para desinstalar a Renderização de imagem em um sistema Linux ou Solaris.
seo-description: Siga estas instruções para desinstalar a Renderização de imagem em um sistema Linux ou Solaris.
seo-title: Desinstalação no Linux e no Solaris
solution: Experience Manager
title: Desinstalação no Linux e no Solaris
uuid: 80c0d6ec-985b-4596-bd67-22e5029f7b37
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '146'
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



