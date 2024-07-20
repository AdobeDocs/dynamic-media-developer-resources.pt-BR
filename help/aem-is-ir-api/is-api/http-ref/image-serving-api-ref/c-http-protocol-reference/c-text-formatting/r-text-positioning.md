---
title: Posicionamento do texto
description: O renderizador text= posiciona o texto de forma fundamentalmente diferente do renderizador textPs= quando aplicado a camadas pré-dimensionadas (ou seja, quando size= também é especificado).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Posicionamento do texto{#text-positioning}

O renderizador `text=` posiciona o texto de forma fundamentalmente diferente do renderizador textPs= quando aplicado a camadas pré-dimensionadas (ou seja, quando size= também é especificado).

As camadas `text=` e `textPs=` de autodimensionamento têm aparência e posicionamento semelhantes.

O `textPs=` alinha a parte superior da célula de caractere com a parte superior da caixa de texto (supondo `\vertalt`), mesmo que resulte em partes dos glifos de texto renderizados se estendendo parcialmente fora do limite da caixa de texto. Os glifos renderizados de determinadas fontes também podem sobressair um pouco além das bordas esquerda e direita da caixa de texto. Para aplicativos que exigem que todo o texto renderizado esteja contido no retângulo de camada, os comandos RTF `\marg*` ou `textFlowPath=` podem ser usados para ajustar a área de renderização do texto.

Por outro lado, o `text=` desloca o texto renderizado conforme necessário e garante que todos os glifos renderizados se encaixem completamente na caixa de texto especificada.

Embora o `text=` seja um pouco mais fácil de usar em aplicativos simples, o `textPs=` oferece posicionamento preciso, independente de faces de fontes e efeitos de texto.

## Exemplos {#section-1b6bdf2ea34447528188ae4e1430ee71}

Os exemplos a seguir são para texto pré-dimensionado. O comportamento do texto de autodimensionamento é diferente.

** `Text=` sempre fornece uma margem estreita no topo:**

![Exemplo de posicionamento de texto em uma imagem](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` renderiza o texto alinhado à parte superior da caixa de texto, o que resulta em um pequeno recorte, mesmo em fontes comuns, como Arial®:**

![Exemplo de posicionamento de texto de duas imagens](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` desloca automaticamente o texto renderizado para baixo para evitar recorte:**

![Exemplo de posicionamento de texto três imagens](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` não move texto contendo partes elevadas, resultando em recorte significativo se o texto estiver na camada 0:**

![Exemplo de posicionamento de texto para quatro imagens](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**Uma margem de 10 pt (200 twips) na parte superior renderiza este texto sem recorte:**

![Exemplo de posicionamento de texto cinco imagens](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**Os glifos renderizados de determinadas fontes de script podem estender-se significativamente fora da caixa de texto:**

![Exemplo de posicionamento de texto seis imagens](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
