---
description: Este tópico descreve a sintaxe de uso da vntc.
seo-description: Este tópico descreve a sintaxe de uso da vntc.
seo-title: Uso
solution: Experience Manager
title: Uso
uuid: 251aa1a0-5f19-42ab-b237-3e3b53fe8320
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---


# Uso{#usage}

Este tópico descreve a sintaxe de uso da vntc.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* é o caminho e o nome do arquivo a ser processado. Pode ser um caminho relativo ao diretório de trabalho atual ou um caminho absoluto. Deve ser uma vinheta válida, um estilo de gabinete ou uma janela que cubra o arquivo de estilo e ter um destes sufixos: [!DNL .vnt], [!DNL .vnc] ou [!DNL .vnw]. Obrigatório.

*[!DNL destFile]* é o caminho e o nome do arquivo de vinheta de saída. Se não especificado, o arquivo de saída é colocado na pasta especificada com `-destpath`. Nesse cenário, o nome do arquivo é gerado automaticamente pelo nome do arquivo de entrada e um sufixo de tamanho, separados pela string especificada com `-separator`. Para vinhetas, o sufixo de tamanho é a largura de pixel da vinheta de saída de resolução única, a largura da primeira exibição de uma vinheta de saída de multiresolução ou &#39;0&#39; no caso de uma vinheta pirâmide. Para arquivos de estilo de gabinete, a resolução de saída é usada como o sufixo do arquivo. *[!DNL destFile]* é ignorada quando  `-info` é especificada.
