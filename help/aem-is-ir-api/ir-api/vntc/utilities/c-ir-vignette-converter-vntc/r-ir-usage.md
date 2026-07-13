---
title: Uso
description: Este tópico descreve a sintaxe de uso do vntc.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
TQID: 'https://experienceleague.adobe.com/uNh-n1OEJ5gxWBjLbBNutrNJ1Osae-PEOFBmaKNVf6c'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 161
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

*[!DNL destFile]* é o caminho e o nome do arquivo de vinheta de saída. Se não for especificado, o arquivo de saída será colocado na pasta especificada com `-destpath`. Nesse cenário, o nome do arquivo é gerado automaticamente a partir do nome do arquivo de entrada e de um sufixo de tamanho, separado com a cadeia de caracteres especificada com `-separator`. Para vinhetas, o sufixo de tamanho é a largura em pixels da vinheta de saída de resolução única, a largura da primeira vista de uma vinheta de saída de várias resoluções ou &quot;0&quot; se houver uma vinheta em pirâmide. Para arquivos de estilo do gabinete, a resolução de saída é usada como o sufixo do arquivo. *[!DNL destFile]* é ignorado quando `-info` é especificado.

