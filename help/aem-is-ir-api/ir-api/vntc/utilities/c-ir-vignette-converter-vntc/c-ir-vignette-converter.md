---
description: O Conversor de vinheta (vntc) é um utilitário de linha de comando usado para preparar o conteúdo criado com a Criação de imagem para implantação com a Renderização de imagem.
seo-description: O Conversor de vinheta (vntc) é um utilitário de linha de comando usado para preparar o conteúdo criado com a Criação de imagem para implantação com a Renderização de imagem.
seo-title: Conversor de vinhetas
solution: Experience Manager
title: Conversor de vinhetas
uuid: b32a30d6-ae4a-406f-88a9-e8b0eec394c9
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---


# Conversor de vinhetas{#vignette-converter}

O Conversor de vinheta (vntc) é um utilitário de linha de comando usado para preparar o conteúdo criado com a Criação de imagem para implantação com a Renderização de imagem.

[!DNL vntc] está localizado em [!DNL  *[!DNL install_root]*\ImageServing\bin]. Ele tem os seguintes recursos:

* Converte as vinhetas primárias em vinhetas de produção de resolução única, multiresolução ou pirâmide (consulte [Escalonamento de vinheta](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Produz gabinete de produção e arquivos de estilo de cobertura de janela (consulte `-resolution` e `-jpegquality`).

* Pode produzir diferentes versões de arquivo de vinhetas, gabinetes e arquivos de estilo de cobertura de janela para uso com versões mais antigas da Renderização de imagem.
* Extrai imagens de visualização de vinhetas, com resolução completa ou miniaturas (consulte `-thumbwidth` e `-image`).
* Extrai propriedades relevantes do arquivo de origem (consulte `-info`) e as envia para `stdout` ou para um arquivo de log opcional (consulte `-log`).

Embora o uso de [!DNL vntc] seja opcional, é altamente recomendável para um melhor desempenho do servidor. [!DNL vntc] também implementa a verificação de erros extensiva e pode evitar problemas graves do servidor, incluindo falhas, quando usado diligentemente.

Ao gerar vinhetas de produção, a largura de pixels da vinheta de saída (ou 0 no caso de pirâmide ou vinhetas de várias resoluções) é anexada ao nome do arquivo de vinheta de saída gerado. Ao processar arquivos de estilo de gabinete, a resolução de saída é anexada ao nome do arquivo de saída. Todos os arquivos de saída, incluindo os arquivos opcionais de miniatura, imagem e log, bem como a vinheta de produção ou o arquivo de estilo de gabinete, são colocados no mesmo diretório em que *[!DNL sourceFile]* está localizado (a menos que `-destPath` seja especificado).

[!DNL vntc] limita-se, por padrão, a no máximo 3 GB de memória. Quando a Vntc atinge esse limite, o processamento será interrompido e gerará um erro. Esse limite pode ser alterado usando `-maxmem`.

>[!NOTE]
>
>A Ferramenta de atualização de vinheta na criação de imagens também pode ser usada para preparar vinhetas para o uso da Renderização de imagens. Da mesma forma, a Ferramenta de criação de conteúdo é capaz de gerar arquivos de estilo de gabinete para uso com a Renderização de imagem. Use [!DNL vntc] se o processamento for automatizado. As ferramentas na Criação de imagens incluem uma interface gráfica do usuário, portanto, normalmente são mais fáceis de usar de forma interativa.

## Consulte também {#section-3c756bf17b634543904fdd928adeafb2}

Documentação de criação de imagem
