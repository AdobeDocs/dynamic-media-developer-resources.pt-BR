---
description: Modelos podem ser usados para reduzir o comprimento e a complexidade das solicitações que compõe várias camadas de imagem ou que incluem texto formatado em rtf.
solution: Experience Manager
title: Modelos
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# Modelos{#templates}

Modelos podem ser usados para reduzir o comprimento e a complexidade das solicitações que compõe várias camadas de imagem ou que incluem texto formatado em rtf.

As variáveis personalizadas podem ser usadas para simplificar ainda mais o uso do modelo. Geralmente, os modelos são configurados para permitir a fácil troca de imagens ou texto ou a definição de outras opções no tempo de execução.

Os modelos são armazenados como registros em catálogos de imagens, com o corpo do modelo no campo `catalog::Modifier` e o campo `catalog::Path` vazio ou especificando uma imagem de plano de fundo estática que não pode ser alterada dinamicamente.

Os modelos são especificados com o comando `template=` ou no componente de caminho do URL da solicitação. Para a maioria dos aplicativos, é recomendável usar o comando `template=` para especificar modelos. O comando `template=`não deve ocorrer no campo `catalog::PostModifier` e só pode ocorrer no campo `catalog::Modifier` em uma solicitação IS aninhada (ou seja, em uma construção `src=is{...}`). Os registros de modelo não podem ser referenciados nos comandos `src=` ou `mask=`.

Qualquer comando `src=` ou `mask=`incorporado no modelo pode resolver o catálogo principal da solicitação ou para um catálogo de imagem diferente. Se nenhum `rootId` for especificado explicitamente, o catálogo principal será considerado. O modelo especificado com `template=` também pode estar localizado no catálogo principal ou em um catálogo de imagem diferente.

É altamente recomendável sempre incluir definições padrão para todas as variáveis usadas em um modelo. Dessa forma, a saída da imagem do modelo sempre pode ser visualizada simplesmente especificando seus `attribute::RootId` e `catalog::Id`, sem precisar saber quais variáveis são usadas no modelo.

A variável de substituição de caminho predefinida `$object$` pode ser usada para aplicar o objeto de imagem especificado no caminho de url a qualquer fonte ou máscara de camada ( `src=` ou `mask=`), mesmo em solicitações aninhadas ou incorporadas.

* [Exemplo A](r-example-a.md)
* [Exemplo B](r-example-b.md)
* [Exemplo C](r-example-c.md)
