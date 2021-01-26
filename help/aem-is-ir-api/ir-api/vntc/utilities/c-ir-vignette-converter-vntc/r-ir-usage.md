---
description: Este tópico descreve a sintaxe de uso de vntc.
seo-description: Este tópico descreve a sintaxe de uso de vntc.
seo-title: Uso
solution: Experience Manager
title: Uso
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 251aa1a0-5f19-42ab-b237-3e3b53fe8320
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# Uso{#usage}

Este tópico descreve a sintaxe de uso de vntc.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* é o caminho e o nome do arquivo a ser processado. Pode ser um caminho relativo ao diretório de trabalho atual ou um caminho absoluto. Deve ser uma vinheta válida, um estilo de gabinete ou um arquivo de estilo de cobertura de janela e ter um destes sufixos: [!DNL .vnt], [!DNL .vnc] ou [!DNL .vnw]. Obrigatório.

*[!DNL destFile]* é o caminho e o nome do arquivo de saída da vinheta. Se não for especificado, o arquivo de saída será colocado na pasta especificada com `-destpath`. Nesse cenário, o nome do arquivo é gerado automaticamente a partir do nome do arquivo de entrada e de um sufixo de tamanho, separados pela string especificada com `-separator`. Para vinhetas, o sufixo de tamanho é a largura em pixels da vinheta de saída de resolução única, a largura da primeira visualização de uma vinheta de saída de multiresolução ou &quot;0&quot; no caso de uma vinheta pirâmide. Para arquivos de estilo de gabinete, a resolução de saída é usada como o sufixo de arquivo. *[!DNL destFile]* é ignorada quando  `-info` é especificada.
