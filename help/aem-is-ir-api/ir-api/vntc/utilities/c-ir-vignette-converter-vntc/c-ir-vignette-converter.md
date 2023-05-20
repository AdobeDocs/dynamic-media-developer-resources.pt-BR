---
description: O Conversor de Vinheta (vntc) é um utilitário de linha de comando usado para preparar o conteúdo criado com a Criação de imagem para implantação com a Renderização de imagem.
solution: Experience Manager
title: Conversor de vinheta
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Conversor de vinheta{#vignette-converter}

O Conversor de Vinheta (vntc) é um utilitário de linha de comando usado para preparar o conteúdo criado com a Criação de imagem para implantação com a Renderização de imagem.

[!DNL vntc] está localizado em [!DNL *[!DNL install_root]*\ServidorDeImagens\bin]. Ele tem os seguintes recursos:

* Converte vinhetas primárias em vinhetas de produção com resolução única, com várias resoluções ou em pirâmide (consulte [Escala de Vinheta](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Produz arquivos de estilo de gabinete de produção e janela (consulte `-resolution` e `-jpegquality`).

* Pode produzir diferentes versões de arquivos de vinhetas, gabinetes e arquivos de estilo de coberturas de janelas para uso com versões mais antigas de Renderização de imagem.
* Extrai as imagens de visualização das vinhetas, seja em resolução completa ou em miniaturas (veja `-thumbwidth` e `-image`).
* Extrai propriedades relevantes do arquivo de origem (consulte `-info`) e os envia para o `stdout` ou um arquivo de registro opcional (consulte `-log`).

Embora a utilização de [!DNL vntc] é opcional, é altamente recomendado para obter o melhor desempenho do servidor. [!DNL vntc] O também implementa uma verificação extensa de erros e pode evitar problemas graves do servidor, incluindo falhas, quando usado com diligência.

Ao gerar vinhetas de produção, a largura em pixels da vinheta de saída (ou 0 no caso de vinhetas em pirâmide ou multiresolução) é anexada ao nome do arquivo de vinheta de saída gerado. Ao processar arquivos de estilo de gabinete, a resolução de saída é anexada ao nome do arquivo de saída. Todos os arquivos de saída, incluindo os arquivos opcionais de miniatura, imagem e log, bem como a vinheta de produção ou o arquivo de estilo do gabinete, são colocados no mesmo diretório em que *[!DNL sourceFile]* está localizado (a menos que `-destPath` é especificado).

[!DNL vntc] O se limita por padrão a no máximo 3 GB de memória. Quando o Vntc atingir esse limite, ele parará de processar e produzirá um erro. Esse limite pode ser alterado usando `-maxmem`.

>[!NOTE]
>
>A Ferramenta de atualização de vinheta na criação de imagens também pode ser usada para preparar vinhetas para o uso de Renderização de imagem. Da mesma forma, a ferramenta de criação de conteúdo é capaz de gerar arquivos de estilo de gabinete para uso com a renderização de imagem. Uso [!DNL vntc] se o processamento for automatizado. As ferramentas de Criação de imagens incluem uma interface gráfica, portanto, são normalmente mais fáceis de usar interativamente.

## Consulte também {#section-3c756bf17b634543904fdd928adeafb2}

Documentação de criação de imagem
