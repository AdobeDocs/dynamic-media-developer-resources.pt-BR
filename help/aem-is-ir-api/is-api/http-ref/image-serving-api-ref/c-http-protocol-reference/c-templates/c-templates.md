---
description: Os modelos podem ser usados para reduzir o comprimento e a complexidade de solicitações que compõe várias camadas de imagem ou que incluem texto formatado em rtf.
seo-description: Os modelos podem ser usados para reduzir o comprimento e a complexidade de solicitações que compõe várias camadas de imagem ou que incluem texto formatado em rtf.
seo-title: Modelos
solution: Experience Manager
title: Modelos
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 54830d1f-40ad-4bf2-8e3d-d3e4d4ab57b9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---


# Modelos{#templates}

Os modelos podem ser usados para reduzir o comprimento e a complexidade de solicitações que compõe várias camadas de imagem ou que incluem texto formatado em rtf.

As variáveis personalizadas podem ser usadas para simplificar ainda mais o uso do modelo. Normalmente, os modelos são configurados para permitir a troca fácil de imagens ou texto ou a configuração de outras opções em tempo de execução.

Os modelos são armazenados como registros em catálogos de imagens, com o corpo do modelo no campo `catalog::Modifier` e o campo `catalog::Path` vazio ou especificando uma imagem de plano de fundo estática que não pode ser alterada dinamicamente.

Os modelos são especificados com o comando `template=` ou no componente de caminho do URL da solicitação. Para a maioria dos aplicativos, é recomendável usar o comando `template=` para especificar modelos. O comando `template=`não deve ocorrer no campo `catalog::PostModifier` e só pode ocorrer no campo `catalog::Modifier` em uma solicitação IS aninhada (isto é, em uma construção `src=is{...}`). Os registros de modelo não podem ser referenciados nos comandos `src=` ou `mask=`.

Qualquer comando `src=` ou `mask=`incorporado no modelo pode ser resolvido para o catálogo principal da solicitação ou para um catálogo de imagens diferente. Se nenhum `rootId` for especificado explicitamente, o catálogo principal será considerado. O modelo especificado com `template=` também pode estar localizado no catálogo principal ou em um catálogo de imagens diferente.

É altamente recomendável sempre incluir definições padrão para todas as variáveis usadas em um modelo. Dessa forma, a saída de imagem do modelo sempre pode ser visualizada simplesmente especificando seus `attribute::RootId` e `catalog::Id`, sem precisar saber quais variáveis são usadas no modelo.

A variável predefinida de substituição de caminho `$object$` pode ser usada para aplicar o objeto de imagem especificado no caminho de url a qualquer fonte de camada ou máscara ( `src=` ou `mask=`), mesmo em solicitações aninhadas ou incorporadas.

* [Exemplo A](r-example-a.md)
* [Exemplo B](r-example-b.md)
* [Exemplo C](r-example-c.md)
