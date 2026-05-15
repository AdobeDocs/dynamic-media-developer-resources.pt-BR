---
title: Modelos
description: Os modelos podem ser usados para reduzir o comprimento e a complexidade de solicitações que compõem várias camadas de imagem ou que incluem texto formatado em rtf.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
TQID: 'https://experienceleague.adobe.com/FFRoxO7iVDzE7Kta5Vig4RtaPWa890tNHPwsAOcWVCw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 300
ht-degree: 0%

---

# Modelos{#templates}

Os modelos podem ser usados para reduzir o comprimento e a complexidade de solicitações que compõem várias camadas de imagem ou que incluem texto formatado em rtf.

As variáveis personalizadas podem ser usadas para simplificar ainda mais o uso do modelo. Geralmente, os modelos são configurados para permitir uma fácil troca de imagens ou texto ou a configuração de outras opções no tempo de execução.

Os modelos são armazenados como registros em catálogos de imagens, com o corpo do modelo no campo `catalog::Modifier` e o campo `catalog::Path` vazio ou especificando uma imagem de fundo estática que não pode ser alterada dinamicamente.

Os modelos são especificados com o comando `template=` ou no componente de caminho da URL de solicitação. Para a maioria dos aplicativos, é recomendável usar o comando `template=` para especificar modelos. O comando `template=` não deve ocorrer no campo `catalog::PostModifier` e só pode ocorrer no campo `catalog::Modifier` em uma solicitação IS aninhada (ou seja, em uma construção `src=is{...}`). Os registros de modelo não podem ser referenciados em `src=` ou `mask=` comandos.

Quaisquer comandos `src=` ou `mask=` inseridos no modelo podem ser resolvidos no catálogo principal da solicitação ou em um catálogo de imagens diferente. Se nenhum `rootId` for especificado explicitamente, o catálogo principal será presumido. O modelo especificado com `template=` também pode estar localizado no catálogo principal ou em um catálogo de imagens diferente.

É altamente recomendável sempre incluir definições padrão para todas as variáveis usadas em um modelo. Dessa forma, a saída de imagem do modelo sempre pode ser visualizada simplesmente especificando seus `attribute::RootId` e `catalog::Id`, sem precisar saber quais variáveis são usadas no modelo.

A variável de substituição de caminho predefinida `$object$` pode ser usada para aplicar o objeto de imagem especificado no caminho da url a qualquer origem ou máscara de camada ( `src=` ou `mask=`), mesmo em solicitações aninhadas ou inseridas.

* [Exemplo A](r-example-a.md)
* [Exemplo B](r-example-b.md)
* [Exemplo C](r-example-c.md)
