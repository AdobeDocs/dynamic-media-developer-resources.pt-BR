---
description: A lista de caminhos, delimitada por ponto e vírgula, serve como raízes para todos os arquivos de dados com caminhos de arquivo relativos.
solution: Experience Manager
title: Pastas raiz do recurso (ir.resourceRootPaths)
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---


# Pastas raiz do recurso (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

A lista de caminhos, delimitada por ponto e vírgula, serve como raízes para todos os arquivos de dados com caminhos de arquivo relativos.

Pode ser caminhos absolutos ou caminhos relativos a *[!DNL install_folder]*. Quando vários caminhos forem especificados, o servidor tentará cada raiz na ordem especificada até que o arquivo seja encontrado. O padrão é [!DNL ./resources], para um caminho raiz padrão de [!DNL install_folder/resources].
