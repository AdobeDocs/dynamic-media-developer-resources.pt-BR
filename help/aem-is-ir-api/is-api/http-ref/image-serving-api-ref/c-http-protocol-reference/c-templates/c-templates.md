---
title: Modelos
description: Modelos podem ser usados para reduzir o comprimento e a complexidade das solicitações que compõe várias camadas de imagem ou que incluem texto formatado em rtf.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Modelos{#templates}

Modelos podem ser usados para reduzir o comprimento e a complexidade das solicitações que compõe várias camadas de imagem ou que incluem texto formatado em rtf.

As variáveis personalizadas podem ser usadas para simplificar ainda mais o uso do modelo. Geralmente, os modelos são configurados para permitir a fácil troca de imagens ou texto ou a definição de outras opções no tempo de execução.

Os modelos são armazenados como registros em catálogos de imagens, com o corpo do modelo na variável `catalog::Modifier` e o `catalog::Path` campo vazio ou especificação de uma imagem de plano de fundo estática que não pode ser alterada dinamicamente.

Os modelos são especificados com a variável `template=` ou no componente de caminho do URL da solicitação. Para a maioria dos aplicativos, é recomendável usar o `template=` para especificar modelos. O `template=`não deve ocorrer no `catalog::PostModifier` e só pode ocorrer no `catalog::Modifier` em uma solicitação IS aninhada (ou seja, em um `src=is{...}` construir). Os registros do modelo não podem ser referenciados em `src=` ou `mask=`comandos.

Qualquer `src=` ou `mask=`os comandos incorporados no modelo podem resolver para o catálogo principal da solicitação ou para um catálogo de imagens diferente. Se não `rootId` for especificado explicitamente, o catálogo principal será considerado. O modelo especificado com `template=` também pode estar localizado no catálogo principal ou em um catálogo de imagem diferente.

É altamente recomendável sempre incluir definições padrão para todas as variáveis usadas em um modelo. Dessa forma, a saída da imagem do modelo sempre pode ser visualizada simplesmente especificando seu `attribute::RootId` e `catalog::Id`, sem precisar saber quais variáveis são usadas no modelo.

A variável de substituição de caminho predefinida `$object$` pode ser usada para aplicar o objeto de imagem especificado no caminho do url a qualquer fonte ou máscara de camada ( `src=` ou `mask=`), mesmo em solicitações aninhadas ou incorporadas.

* [Exemplo A](r-example-a.md)
* [Exemplo B](r-example-b.md)
* [Exemplo C](r-example-c.md)
