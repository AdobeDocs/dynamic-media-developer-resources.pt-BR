---
description: Crie um aplicativo de camadas "papel doll".
seo-description: Crie um aplicativo de camadas "papel doll".
seo-title: Exemplo C
solution: Experience Manager
title: Exemplo C
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 25f228c2-dc03-461a-aee8-40fdb3d4cf5e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---


# Exemplo C{#example-c}

Crie um aplicativo de camadas &quot;papel doll&quot;.

Uma imagem de plano de fundo contém a foto de um modelo ou de um manequim. Registros adicionais no catálogo de imagens contêm vários itens de vestuário e acessórios, fotografados para corresponder ao manequim na forma e no tamanho.

Cada foto de aparato/acessório é mascarada e cortada na caixa delimitadora de máscara para minimizar os tamanhos de imagem. As âncoras e resoluções de imagens são cuidadosamente controladas para manter o alinhamento entre as camadas e a imagem de plano de fundo, e todas as imagens são adicionadas a um catálogo de imagens, com os valores apropriados armazenados em `catalog::Resolution` e `catalog::Anchor`.

Além da disposição em camadas, também queremos alterar a cor dos itens selecionados. Os registros desses itens são pré-processados para remover a cor original e ajustar o brilho e o contraste de forma adequada ao comando de colorização. Esse pré-processamento pode ser feito offline, usando uma ferramenta de edição de imagem como Photoshop, ou, em casos simples, pode ser feito trivialmente adicionando `op_brightness=` e `op_contrast=` ao campo `catalog::Modifier`.

Este aplicativo não garante um modelo separado, pois todos os objetos já estão alinhados corretamente por suas âncoras de imagem ( `catalog::Anchor`) e dimensionados ( `catalog::Resolution`). Deixamos para o cliente garantir a ordem de camadas apropriada.

Uma solicitação típica pode ser parecida com esta:

```
http://server/rootId/mannequin?&hei=400&qlt=90&
layer=1&res=999&src=rootId/tankTopGeneric&colorize=240,122,17&
 layer=2&res=999&src=rootId/skirt14a&
layer=3&res=999&src=rootId/jacket09&
layer=4&res=999&src=rootId/hat2generic&colorize=12,15,34&
 layer=5&res=999&src=rootId/sunglasses&
layer=6&res=999&src=rootId/shoes21
```

Somente a altura é especificada. Isso permite que a imagem retornada varie na largura, dependendo da proporção da imagem de manequim, sem obter margens preenchidas com a cor de plano de fundo.

Não importa qual resolução é especificada para cada camada, desde que todas sejam iguais. Esta versão pode não permitir que as visualizações sejam maiores que as imagens compostas. A especificação de um valor de resolução grande evita problemas relacionados a essa limitação. Todo o processamento e composição são feitos na resolução ideal para o tamanho de imagem solicitado, para ajudar a obter o melhor desempenho e qualidade de saída.

Os comandos `res=` podem ser omitidos se todas as imagens de origem tiverem a mesma resolução em escala completa (o que provavelmente acontece com esse tipo de aplicativo).

Os `rootId` devem ser especificados para todos os comandos `src=`, mesmo que sejam os mesmos que `rootId` especificados no caminho de url.

Se nenhum catálogo de imagens for usado, uma abordagem baseada em resolução para dimensionamento não será possível. Nesse caso, fatores de escala explícitos devem ser calculados para cada item de camada, com base na proporção dos valores `catalog::Resolution` para cada camada com o valor `catalog::Resolution` da camada de plano de fundo. A solicitação de composição (com menos camadas) pode, portanto, ter a seguinte aparência:

```
http://server/myApp/mannequin.tif?&hei=400&qlt=90&
 layer= 1&scale=0.3423&anchor=345,225&src=myApp/images/tankTopGeneric.tif&colorize=240,122,17&
 layer=2&scale=0.8544&anchor=140,-157&src=myApp/images/skirt14a
```

