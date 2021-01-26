---
description: A especificação RTF permite valores de cor RGB especificados com &bsol;colortbl. Cada componente é fornecido separadamente com os comandos &bsol;red, &bsol;green e &bsol;blue.
solution: Experience Manager
title: Tratamento de cores
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6c51d204-27ca-4fbd-a297-bf1d04b63a3f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---


# Tratamento de cores{#color-handling}

A especificação RTF permite valores de cor RGB especificados com `\colortbl`. Cada componente é fornecido separadamente com os comandos `\red`, `\green` e `\blue`.

O comando proprietário de extensão RTF `\cmykcolortbl` permite especificar cores CMYK, com cada componente de cor fornecido com os comandos `\cyan`, `\magenta`, `\yellow` e `\black`.

Os valores dos componentes coloridos para `\colortbl` estão no intervalo de 0 a 255. Os valores dos componentes para `\cmykcolortbl` estão no intervalo de 0 a 100.

O comando de extensão RTF `\*\iscolortbl`, suportado por `textPs=`, fornece uma maneira de especificar uma tabela colorida com valores de cor padrão do Serviço de Imagens, com suporte total a RGB, cinza, CMYK e alfa. Ela tem a seguinte sintaxe:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* um ou mais valores de cor IS, separados por &#39;;&#39;

É possível especificar mais de um tipo de tabela colorida na mesma sequência de caracteres `text=` ou `textPs=` RTF. Cada tabela de cores pode ter um número diferente de entradas. O Serviço de Imagens tentará localizar cores nesta ordem: `\iscolortbl` antes de `\cmykcolortbl` (somente se o tipo de pixel da camada de texto for CMYK) antes de `\colortbl`. Somente para `textPs=`, as cores são convertidas com precisão entre CMYK e RGB, se necessário (por exemplo, quando as cores RGB são especificadas, mas a saída CMYK é necessária). Se nenhuma cor para um valor de índice específico for encontrada, a cor padrão (preto) será usada.

Consulte [color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) para obter uma descrição da sintaxe dos valores de cor IS.

## Restrições {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` não suporta  `\*\iscolortbl`. `textPs=` não suporta  `\cmykcolortbl`.

As seleções de cores são ignoradas ao renderizar fontes de fotos.

## Exemplo {#section-0f166bb72bd44479be01131077851142}

Permita que três cores de texto sejam controladas com variáveis, enquanto ainda exibe o valor padrão de cor quando a string RTF é aberta em um editor de texto RTF padrão.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
