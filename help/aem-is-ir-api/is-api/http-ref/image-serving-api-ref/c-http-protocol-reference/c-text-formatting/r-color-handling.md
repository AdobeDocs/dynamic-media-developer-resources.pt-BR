---
description: A especificação RTF permite valores de cor de RGB especificados com &bsol;colortbl. Cada componente é fornecido separadamente com os comandos &bsol;red, &bsol;green e &bsol;blue.
solution: Experience Manager
title: Tratamento de cores
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Tratamento de cores{#color-handling}

A especificação RTF permite valores de cor de RGB especificados com `\colortbl`. Cada componente é fornecido separadamente com o `\red`, `\green`, e `\blue` comandos.

O comando de extensão RTF proprietário `\cmykcolortbl` permite especificar cores CMYK, com cada componente de cor fornecido com o `\cyan`, `\magenta`, `\yellow`, e `\black` comandos.

Valores do componente de cor para `\colortbl` estão no intervalo de 0 a 255. Valores de componente para `\cmykcolortbl` estão no intervalo de 0 a 100.

O comando de extensão RTF `\*\iscolortbl`, com suporte do `textPs=`, fornece uma maneira de especificar uma tabela de cores com valores de cores padrão do Servidor de imagens, com suporte completo para RGB, cinza, CMYK e alfa. Ela tem a seguinte sintaxe:

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* um ou mais valores de cor IS, separados por &#39;;&#39;

Mais de um tipo de tabela de cores pode ser especificada na mesma `text=` ou `textPs=` String RTF. Cada tabela de cores pode ter um número diferente de entradas. O Servidor de imagens tentará encontrar cores nesta ordem: `\iscolortbl` antes `\cmykcolortbl` (somente se o tipo de pixel da camada de texto for CMYK) antes de `\colortbl`. Para `textPs=` somente, as cores são convertidas com precisão entre CMYK e RGB, se necessário (por exemplo, quando as cores de RGB são especificadas, mas a saída CMYK é necessária). Se nenhuma cor para um determinado valor de índice for encontrada, a cor padrão (preto) será usada.

Consulte [cor](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) para obter uma descrição da sintaxe dos valores de cor IS.

## Restrições {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` não suporta `\*\iscolortbl`. `textPs=` não suporta `\cmykcolortbl`.

As seleções de cores são ignoradas ao renderizar as fontes fotográficas.

## Exemplo {#section-0f166bb72bd44479be01131077851142}

Permite que três cores de texto sejam controladas com variáveis, enquanto ainda exibe o valor padrão da cor quando a cadeia de caracteres RTF é aberta em um editor de texto RTF padrão.

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
