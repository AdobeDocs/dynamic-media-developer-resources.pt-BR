---
title: Pastas raiz do recurso (ir.resourceRootPaths)
description: Uma lista de caminhos, delimitada por ponto e vírgula, serve como raiz para todos os arquivos de dados com caminhos de arquivo relativos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 49fd45da-1af9-4016-8fc6-6ec17b7e553b
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---

# Pastas raiz do recurso (ir.resourceRootPaths){#resource-root-folders-ir-resourcerootpaths}

Uma lista de caminhos, delimitada por ponto e vírgula, serve como raiz para todos os arquivos de dados com caminhos de arquivo relativos.

Eles podem ser caminhos absolutos ou caminhos relativos a *[!DNL install_folder]*. Quando vários caminhos são especificados, o servidor tenta cada raiz na ordem especificada até que o arquivo seja encontrado. O padrão é [!DNL ./resources], para um caminho raiz padrão de [!DNL install_folder/resources].
