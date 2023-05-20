---
title: Exemplo C
description: Crie um aplicativo em camadas de "boneca de papel".
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 70232055-2a4c-4e56-8076-3cd56a9004c5
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Exemplo C{#example-c}

Crie um aplicativo em camadas de &quot;boneca de papel&quot;.

Uma imagem de fundo contém a foto de um modelo ou manequim. Registros adicionais no catálogo de imagens contêm vários artigos de vestuário e acessórios, fotografados para corresponder ao manequim em forma e tamanho.

Cada foto de vestuário/acessório é mascarada e cortada na caixa delimitadora de máscara para minimizar os tamanhos de imagem. As âncoras e resoluções de imagem são cuidadosamente controladas para manter o alinhamento entre as camadas e a imagem de plano de fundo, e todas as imagens são adicionadas a um catálogo de imagens, com os valores apropriados armazenados no `catalog::Resolution` e `catalog::Anchor`.

Além da disposição em camadas, também é necessário alterar a cor dos itens selecionados. Os registros desses itens são pré-processados para remover a cor original e ajustar o brilho e o contraste de uma forma adequada para o comando de coloração. Esse pré-processamento pode ser feito off-line, usando uma ferramenta de edição de imagens, como o Adobe Photoshop, ou, em casos simples, pode ser feito trivialmente adicionando `op_brightness=` e `op_contrast=` para o `catalog::Modifier`campo.

Esse aplicativo não garante um modelo separado, pois todos os objetos já estão alinhados corretamente por suas âncoras de imagem ( `catalog::Anchor`) e dimensionado ( `catalog::Resolution`). Cabe ao cliente garantir a ordem apropriada das camadas.

Uma solicitação típica pode ter esta aparência:

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

Somente a altura é especificada. Isso permite que a imagem retornada varie em largura, dependendo da proporção da imagem do manequim, sem que as margens sejam preenchidas com a cor de fundo.

Não importa qual resolução é especificada para cada camada, desde que todas sejam iguais. Esta versão pode não permitir exibições maiores do que as imagens compostas. Especificar um valor de resolução grande evita problemas relacionados a essa limitação. Todo o processamento e composição é feito na resolução ideal para o tamanho de imagem solicitado, para ajudar a alcançar o melhor desempenho e qualidade de saída.

A variável `res=` os comandos podem ser omitidos se todas as imagens de origem tiverem a mesma resolução em escala completa (o que provavelmente é o caso desse tipo de aplicativo).

A variável `rootId` deve ser especificado para todos `src=` mesmo que sejam os mesmos que os comandos `rootId` especificado no caminho do url.

Se nenhum catálogo de imagens for usado, não será possível uma abordagem de dimensionamento baseada em resolução. Nesse caso, os fatores de escala explícitos devem ser calculados para cada item da camada, com base na proporção do `catalog::Resolution` valores de cada camada para o `catalog::Resolution` valor da camada de plano de fundo. A solicitação de composição (com menos camadas) pode ter esta aparência:

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```
