---
title: Conversor de vinheta
description: O Conversor de Vinheta (vntc) é um utilitário de linha de comando usado para preparar o conteúdo criado com a Criação de imagem para implantação com a Renderização de imagem.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
TQID: 'https://experienceleague.adobe.com/NZsbUGCd25rHyvrmt-Rh3XN0p3pHqEtGZrXLp-7JBsc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 337
ht-degree: 0%

---

# Conversor de vinheta{#vignette-converter}

O Conversor de Vinheta (vntc) é um utilitário de linha de comando usado para preparar o conteúdo criado com a Criação de imagem para implantação com a Renderização de imagem.

[!DNL vntc] está em [!DNL *[!DNL install_root]*\ImageServing\bin]. Ele tem os seguintes recursos:

* Converte vinhetas primárias em vinhetas de produção de resolução única, resolução múltipla ou pirâmide (consulte [Escala de vinheta](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Produz arquivos de estilo de gabinete de produção e janela de cobertura (consulte `-resolution` e `-jpegquality`).

* Produza diferentes versões de arquivos de vinhetas, gabinetes e arquivos de estilo de coberturas de janelas para uso com versões mais antigas de Renderização de imagem.
* Extrai imagens de exibição de vinhetas, em resolução total ou em miniaturas (consulte `-thumbwidth` e `-image`).
* Extrai propriedades relevantes do arquivo de origem (consulte `-info`) e as envia para `stdout` ou para um arquivo de log opcional (consulte `-log`).

Embora o uso do [!DNL vntc] seja opcional, a Adobe recomenda seu uso para obter o melhor desempenho do servidor. O Conversor de vinheta também implementa uma extensa verificação de erros e pode evitar problemas graves do servidor, incluindo falhas, quando usado com diligência.

Ao gerar vinhetas de produção, a largura em pixels da vinheta de saída (ou 0 se for uma pirâmide ou vinheta de várias resoluções) é anexada ao nome do arquivo de vinheta de saída gerado. Ao processar arquivos de estilo de gabinete, a resolução de saída é anexada ao nome do arquivo de saída. Todos os arquivos de saída, incluindo os arquivos opcionais de miniatura, imagem e log e o arquivo de estilo de vinheta ou gabinete de produção são colocados no mesmo diretório em que *[!DNL sourceFile]* está localizado (a menos que `-destPath` seja especificado).

O Conversor de Vinheta limita-se por padrão a no máximo 3 GB de memória. Quando o vntc atinge esse limite, ele interrompe o processamento e produz um erro. Esse limite pode ser alterado usando `-maxmem`.

>[!NOTE]
>
>A Ferramenta de atualização de vinheta na criação de imagens também pode ser usada para preparar vinhetas para o uso de Renderização de imagem. Da mesma forma, a Ferramenta de criação de conteúdo pode gerar arquivos de estilo de gabinete para uso com a Renderização de imagem. Use [!DNL vntc] se o processamento for automatizado. As ferramentas de Criação de imagens incluem uma interface gráfica, portanto, são normalmente mais fáceis de usar interativamente.

## Consulte também {#section-3c756bf17b634543904fdd928adeafb2}

Documentação de criação de imagem
