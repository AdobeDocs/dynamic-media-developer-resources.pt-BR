---
title: Uso
description: Este tópico descreve a sintaxe de uso do vntc.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# Uso{#usage}

Este tópico descreve a sintaxe de uso do vntc.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* é o caminho e o nome do arquivo a ser processado. Pode ser um caminho relativo ao diretório de trabalho atual ou um caminho absoluto. Deve ser uma vinheta válida, um estilo de gabinete ou um arquivo de estilo de cobertura de janela e deve ter um dos seguintes sufixos:

* [!DNL .vnt]
* [!DNL .vnc]
* [!DNL .vnw]

Obrigatório.

*[!DNL destFile]* é o caminho e o nome do arquivo de vinheta de saída. Se não for especificado, o arquivo de saída será colocado na pasta especificada com `-destpath`. Nesse cenário, o nome do arquivo é gerado automaticamente a partir do nome do arquivo de entrada e de um sufixo de tamanho, separado pela cadeia de caracteres especificada com `-separator`. Para vinhetas, o sufixo de tamanho é a largura em pixels da vinheta de saída de resolução única, a largura da primeira vista de uma vinheta de saída de várias resoluções ou &quot;0&quot; se houver uma vinheta em pirâmide. Para arquivos de estilo do gabinete, a resolução de saída é usada como o sufixo do arquivo. *[!DNL destFile]* é ignorado quando `-info` é especificado.
