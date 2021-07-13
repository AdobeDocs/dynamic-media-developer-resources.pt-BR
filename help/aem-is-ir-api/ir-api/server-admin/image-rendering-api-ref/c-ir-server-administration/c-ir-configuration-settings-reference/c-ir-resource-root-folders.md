---
description: A lista de caminhos, delimitada por ponto e vírgula, serve como raízes para todos os arquivos de dados com caminhos de arquivo relativos.
solution: Experience Manager
title: Pastas raiz do recurso (ir.resourceRootPaths)
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---

# Pastas raiz do recurso (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

A lista de caminhos, delimitada por ponto e vírgula, serve como raízes para todos os arquivos de dados com caminhos de arquivo relativos.

Pode ser caminhos absolutos ou caminhos relativos a *[!DNL install_folder]*. Quando vários caminhos forem especificados, o servidor tentará cada raiz na ordem especificada até que o arquivo seja encontrado. O padrão é [!DNL ./resources], para um caminho raiz padrão de [!DNL install_folder/resources].
