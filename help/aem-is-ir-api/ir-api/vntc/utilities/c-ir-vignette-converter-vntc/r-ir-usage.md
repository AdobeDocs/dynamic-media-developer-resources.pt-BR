---
description: Este tópico descreve a sintaxe de uso da vntc.
solution: Experience Manager
title: Uso
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# Uso{#usage}

Este tópico descreve a sintaxe de uso da vntc.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* é o caminho e o nome do arquivo a ser processado. Pode ser um caminho relativo ao diretório de trabalho atual ou um caminho absoluto. Deve ser uma vinheta válida, um estilo de gabinete ou uma janela que cubra o arquivo de estilo e ter um destes sufixos: [!DNL .vnt], [!DNL .vnc] ou [!DNL .vnw]. Obrigatório.

*[!DNL destFile]* é o caminho e o nome do arquivo de vinheta de saída. Se não especificado, o arquivo de saída é colocado na pasta especificada com `-destpath`. Nesse cenário, o nome do arquivo é gerado automaticamente pelo nome do arquivo de entrada e um sufixo de tamanho, separados pela string especificada com `-separator`. Para vinhetas, o sufixo de tamanho é a largura de pixel da vinheta de saída de resolução única, a largura da primeira exibição de uma vinheta de saída de multiresolução ou &#39;0&#39; no caso de uma vinheta pirâmide. Para arquivos de estilo de gabinete, a resolução de saída é usada como o sufixo do arquivo. *[!DNL destFile]* é ignorada quando  `-info` é especificada.
