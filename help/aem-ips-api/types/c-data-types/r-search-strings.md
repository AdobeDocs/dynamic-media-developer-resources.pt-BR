---
description: Pesquisar registro de cadeia de caracteres extraído de um arquivo do PDF.
solution: Experience Manager
title: SearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3f67ba8a-12dd-4698-9502-7cbdec9cb25d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# [!DNL SearchStrings]{#searchstrings}

Pesquisar registro de cadeia de caracteres extraído de um arquivo do PDF.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| searchString | `xsd:string` | Texto da sequência de caracteres de pesquisa. |
| keywordsArray | `types:KeywordsArray` | Matriz de palavras-chave na cadeia de caracteres de pesquisa. |
| status | `xsd:boolean` | True se a cadeia de caracteres de pesquisa for válida e habilitada. |
| x | `xsd:int` | Posição do eixo X da cadeia de caracteres de pesquisa. |
| y | `xsd:int` | Posição do eixo Y da cadeia de caracteres de pesquisa. |
| largura | `xsd:int` | Largura da string de pesquisa. |
| altura | `xsd:int` | Altura da string de pesquisa. |
| fontName | `xsd:string` | Nome da fonte usada na cadeia de caracteres de pesquisa. |
| pointSize | `xsd:string` | Tamanho da fonte. |
