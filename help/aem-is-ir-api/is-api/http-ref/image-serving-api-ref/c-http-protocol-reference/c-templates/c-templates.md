---
title: Modelos
description: Os modelos podem ser usados para reduzir o comprimento e a complexidade de solicitações que compõem várias camadas de imagem ou que incluem texto formatado em rtf.
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

Os modelos podem ser usados para reduzir o comprimento e a complexidade de solicitações que compõem várias camadas de imagem ou que incluem texto formatado em rtf.

As variáveis personalizadas podem ser usadas para simplificar ainda mais o uso do modelo. Geralmente, os modelos são configurados para permitir uma fácil troca de imagens ou texto ou a configuração de outras opções no tempo de execução.

Os modelos são armazenados como registros em catálogos de imagem, com o corpo do modelo no `catalog::Modifier` e a variável `catalog::Path` campo vazio ou especificando uma imagem de fundo estática que não pode ser alterada dinamicamente.

Os modelos são especificados com o `template=` ou no componente de caminho do URL da solicitação. Para a maioria dos aplicativos, é recomendável usar o `template=` para especificar modelos. A variável `template=`comando não deve ocorrer no `catalog::PostModifier` e só pode ocorrer no campo `catalog::Modifier` em uma solicitação IS aninhada (ou seja, em um `src=is{...}` construir). Os registros de modelo não podem ser referenciados em `src=` ou `mask=`comandos.

Qualquer `src=` ou `mask=`Os comandos incorporados no modelo podem ser resolvidos no catálogo principal da solicitação ou em um catálogo de imagens diferente. Se não `rootId` for especificado explicitamente, o catálogo principal será assumido. O modelo especificado com `template=` O também pode estar localizado no catálogo principal ou em um catálogo de imagens diferente.

É altamente recomendável sempre incluir definições padrão para todas as variáveis usadas em um modelo. Dessa forma, a saída de imagem do template sempre pode ser visualizada especificando-se sua `attribute::RootId` e `catalog::Id`, sem precisar saber quais variáveis são usadas no modelo.

A variável de substituição de caminho predefinida `$object$` pode ser usado para aplicar o objeto de imagem especificado no caminho do url a qualquer origem ou máscara de camada ( `src=` ou `mask=`), mesmo em solicitações aninhadas ou incorporadas.

* [Exemplo A](r-example-a.md)
* [Exemplo B](r-example-b.md)
* [Exemplo C](r-example-c.md)
