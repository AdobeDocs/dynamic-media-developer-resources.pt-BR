---
description: Os modelos podem ser usados para reduzir o comprimento e a complexidade de solicitações que compõe várias camadas de imagem ou que incluem texto formatado em rtf.
seo-description: Os modelos podem ser usados para reduzir o comprimento e a complexidade de solicitações que compõe várias camadas de imagem ou que incluem texto formatado em rtf.
seo-title: Modelos
solution: Experience Manager
title: Modelos
topic: Scene7 Image Serving - Image Rendering API
uuid: 54830d1f-40ad-4bf2-8e3d-d3e4d4ab57b9
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# Modelos{#templates}

Os modelos podem ser usados para reduzir o comprimento e a complexidade de solicitações que compõe várias camadas de imagem ou que incluem texto formatado em rtf.

As variáveis personalizadas podem ser usadas para simplificar ainda mais o uso do modelo. Normalmente, os modelos são configurados para permitir a troca fácil de imagens ou texto ou a configuração de outras opções em tempo de execução.

Os modelos são armazenados como registros em catálogos de imagens, com o corpo do modelo no `catalog::Modifier` campo e o `catalog::Path` campo vazio ou especificando uma imagem de plano de fundo estática que não pode ser alterada dinamicamente.

Os modelos são especificados com o `template=` comando ou no componente de caminho do URL da solicitação. Para a maioria dos aplicativos, é recomendável usar o `template=` comando para especificar modelos. O `template=`comando não deve ocorrer no `catalog::PostModifier` campo e só pode ocorrer no `catalog::Modifier` campo em uma solicitação IS aninhada (isto é, em uma `src=is{...}` construção). Os registros de modelo não podem ser referenciados em `src=` ou `mask=`comandos.

Qualquer `src=` ou `mask=`comandos incorporados no modelo podem ser resolvidos para o catálogo principal da solicitação ou para um catálogo de imagens diferente. Se nenhum `rootId` for especificado explicitamente, o catálogo principal será considerado. O modelo especificado com `template=` pode também estar localizado no catálogo principal ou em um catálogo de imagens diferente.

É altamente recomendável sempre incluir definições padrão para todas as variáveis usadas em um modelo. Dessa forma, a saída de imagem do modelo sempre pode ser visualizada simplesmente especificando suas `attribute::RootId` e `catalog::Id`, sem precisar saber quais variáveis são usadas no modelo.

A variável de substituição de caminho predefinida `$object$` pode ser usada para aplicar o objeto de imagem especificado no caminho de url a qualquer fonte de camada ou máscara ( `src=` ou `mask=`), mesmo em solicitações aninhadas ou incorporadas.

* [Exemplo A](r-example-a.md)
* [Exemplo B](r-example-b.md)
* [Exemplo C](r-example-c.md)
