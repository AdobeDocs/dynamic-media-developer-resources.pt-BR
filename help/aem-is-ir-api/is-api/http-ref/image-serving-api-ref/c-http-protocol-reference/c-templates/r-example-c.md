---
description: Crie um aplicativo de camadas de "boneca de papel".
seo-description: Crie um aplicativo de camadas de "boneca de papel".
seo-title: Exemplo C
solution: Experience Manager
title: Exemplo C
uuid: 25f228c2-dc03-461a-aee8-40fdb3d4cf5e
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---


# Exemplo C{#example-c}

Crie um aplicativo de camadas de &quot;boneca de papel&quot;.

Uma imagem de plano de fundo contém a foto de um modelo ou manequim. Registros adicionais no catálogo de imagens contêm vários itens de vestuário e acessórios, fotografados para corresponder ao manequim em forma e tamanho.

Cada foto de vestuário/acessório é mascarada e cortada na caixa delimitadora de máscara para minimizar os tamanhos de imagem. As âncoras e resoluções de imagem são cuidadosamente controladas para manter o alinhamento entre as camadas e a imagem de plano de fundo, e todas as imagens são adicionadas a um catálogo de imagens, com os valores apropriados armazenados em `catalog::Resolution` e `catalog::Anchor`.

Além do layout, também queremos alterar a cor dos itens selecionados. Os registros desses itens são pré-processados para remover a cor original e ajustar o brilho e o contraste de forma adequada ao comando de colorização. Esse pré-processamento pode ser feito off-line, usando uma ferramenta de edição de imagem, como o Photoshop, ou, em casos simples, pode ser feito trivialmente adicionando `op_brightness=` e `op_contrast=` ao campo `catalog::Modifier`.

Este aplicativo não garante um modelo separado, pois todos os objetos já estão alinhados corretamente por suas âncoras de imagem ( `catalog::Anchor`) e dimensionados ( `catalog::Resolution`). Deixamos a responsabilidade do cliente garantir a ordem de camada apropriada.

Uma solicitação típica pode ser semelhante a:

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

Somente a altura é especificada. Isso permite que a imagem retornada varie na largura, dependendo da proporção da imagem do manequim, sem obter margens preenchidas com a cor do fundo.

Não importa qual resolução é especificada para cada camada, desde que sejam todas iguais. Esta versão pode não permitir que as visualizações sejam maiores do que as imagens compostas. Especificar um valor de resolução grande evita problemas relacionados a essa limitação. Todo o processamento e composição são feitos na resolução ideal para o tamanho de imagem solicitado, para ajudar a alcançar o melhor desempenho e qualidade de saída.

Os comandos `res=` podem ser omitidos se todas as imagens de origem tiverem a mesma resolução em escala completa (o que provavelmente acontece com esse tipo de aplicativo).

O `rootId` deve ser especificado para todos os comandos `src=`, mesmo que sejam iguais ao `rootId` especificado no caminho de url.

Se nenhum catálogo de imagem for usado, uma abordagem baseada em resolução para dimensionamento não será possível. Nesse caso, fatores de escala explícitos devem ser calculados para cada item de camada, com base na proporção dos valores `catalog::Resolution` para cada camada com o valor `catalog::Resolution` da camada de plano de fundo. A solicitação de composição (com menos camadas) pode, portanto, ter a seguinte aparência:

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```

