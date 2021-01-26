---
description: O Conversor de vinheta (vntc) é um utilitário de linha de comando usado para preparar o conteúdo criado com a Criação de imagem para implantação com a Renderização de imagem.
seo-description: O Conversor de vinheta (vntc) é um utilitário de linha de comando usado para preparar o conteúdo criado com a Criação de imagem para implantação com a Renderização de imagem.
seo-title: Conversor de vinheta
solution: Experience Manager
title: Conversor de vinheta
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b32a30d6-ae4a-406f-88a9-e8b0eec394c9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---


# Conversor de vinheta{#vignette-converter}

O Conversor de vinheta (vntc) é um utilitário de linha de comando usado para preparar o conteúdo criado com a Criação de imagem para implantação com a Renderização de imagem.

[!DNL vntc] está localizado em [!DNL  *[!DNL install_root]*\ImageServing\bin]. Ele tem os seguintes recursos:

* Converte as vinhetas primárias em vinhetas de produção de resolução única, multiresolução ou pirâmide (consulte [Escala de vinheta](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Produz gabinetes de produção e janelas que abrangem arquivos de estilo (consulte `-resolution` e `-jpegquality`).

* Pode produzir versões de arquivos diferentes de vinhetas, gabinetes e arquivos de estilo de revestimento de janela para uso com versões mais antigas da Renderização de imagem.
* Extrai imagens de visualização de vinhetas, com resolução total ou miniaturas (consulte `-thumbwidth` e `-image`).
* Extrai as propriedades relevantes do arquivo de origem (consulte `-info`) e as envia para `stdout` ou um arquivo de log opcional (consulte `-log`).

Embora o uso de [!DNL vntc] seja opcional, é altamente recomendável para o melhor desempenho do servidor. [!DNL vntc] além disso, implementa uma ampla verificação de erros e pode evitar problemas graves no servidor, incluindo falhas, quando usado de forma diligente.

Ao gerar vinhetas de produção, a largura de pixel da vinheta de saída (ou 0 no caso de pirâmide ou vinhetas de multiresolução) é anexada ao nome do arquivo de vinheta de saída gerado. Ao processar arquivos estilo gabinete, a resolução de saída é anexada ao nome do arquivo de saída. Todos os arquivos de saída, incluindo os arquivos opcionais de miniatura, imagem e registro, bem como o arquivo de estilo de vinheta ou gabinete de produção, são colocados no mesmo diretório em que *[!DNL sourceFile]* está localizado (a menos que `-destPath` seja especificado).

[!DNL vntc] limita-se, por padrão, a no máximo 3 GB de memória. Quando a Vntc atingir esse limite, o processamento será interrompido e ocorrerá um erro. Esse limite pode ser alterado usando `-maxmem`.

>[!NOTE]
>
>A Ferramenta de atualização de vinheta na criação de imagens também pode ser usada para preparar vinhetas para o uso da renderização de imagens. Da mesma forma, a Ferramenta de criação de conteúdo é capaz de gerar arquivos no estilo gabinete para uso com a Renderização de imagem. Use [!DNL vntc] se o processamento for automatizado. As ferramentas na Criação de imagens incluem uma interface gráfica do usuário, portanto, normalmente são mais fáceis de usar interativamente.

## Consulte também {#section-3c756bf17b634543904fdd928adeafb2}

Documentação de criação de imagem
