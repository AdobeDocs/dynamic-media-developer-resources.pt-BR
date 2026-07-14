---
title: Desinstalando no Linux® e Solaris™
description: Siga estas instruções para desinstalar a Renderização de imagem em um sistema Linux® ou Solaris™.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
TQID: 'https://experienceleague.adobe.com/RmD5z5300Nw12kSsOretyAl5p-TeFkox-Cyqm1MrF5w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 120
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


