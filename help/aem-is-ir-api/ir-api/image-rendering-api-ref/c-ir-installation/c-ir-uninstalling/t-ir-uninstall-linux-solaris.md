---
title: Desinstalando no Linux® e Solaris™
description: Siga estas instruções para desinstalar a Renderização de imagem em um sistema Linux® ou Solaris™.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---

# Desinstalando no Linux® e Solaris™{#uninstalling-on-linux-and-solaris}

Siga estas instruções para desinstalar a Renderização de imagem em um sistema Linux® ou Solaris™. Há dois métodos diferentes que você pode usar. Siga um destes procedimentos:

## Método 1

1. Localizar [!DNL uninstall.sh].

   Ela está no diretório no qual o ImageRendering foi instalado. Se este diretório tiver sido removido, o pacote de instalação original deverá ser descompactado e não testado para extrair [!DNL uninstall.sh].
1. Execute [!DNL uninstall.sh] e siga as instruções na tela.

## Método 2

1. Interromper ImageRendering com o seguinte:

   ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`

1. Remova ImageRendering do sistema. O comando usado depende do sistema.
   * Linux®: `rpm -e ImageRendering`

   * Solaris™: `pkgrm ImageRendering`

1. Exclua diretórios ou arquivos que não foram removidos na etapa 2.

