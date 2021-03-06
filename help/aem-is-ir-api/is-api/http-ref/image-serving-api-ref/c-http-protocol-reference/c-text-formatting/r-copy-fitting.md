---
description: textPs= implementa um algoritmo de ajuste de cópia proprietário que ajusta automaticamente os tamanhos de fonte para preencher de maneira ideal a área de texto com texto, minimizando o espaço extra na parte inferior e evitando sobrefluxo.
solution: Experience Manager
title: Montagem de cópias
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1a560f3-f92c-4143-b80a-e1674c8a4207
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# Montagem de cópias{#copy-fitting}

textPs= implementa um algoritmo de ajuste de cópia proprietário que ajusta automaticamente os tamanhos de fonte para preencher de maneira ideal a área de texto com texto, minimizando o espaço extra na parte inferior e evitando sobrefluxo.

O ajuste da cópia pode ser ativado e controlado coletivamente para a camada de texto inteira, com base em parágrafo, mesmo para uma extensão de texto individual.

Especifique o tamanho mínimo da fonte com `\fs` e o tamanho máximo da fonte com `\copyfit`. Qualquer número de intervalos é permitido na mesma string RTF. Os tamanhos de todos os intervalos são variados proporcionalmente, garantindo que as proporções de tamanho de fonte desejadas sejam mantidas.

`\copyfit` é considerado um comando de formatação de caractere e tem regras de escopo como `\fs` e `\b`.

O ajuste da cópia é desativado ao especificar `\copyfit` com um tamanho igual ou inferior ao tamanho especificado com `\fs`.

## Limite do número de linhas {#section-e5aee0f039e04842afc3d6884ed681ac}

Além de especificar o intervalo de tamanhos de fonte, o comportamento do algoritmo de ajuste de cópia pode ser controlado ainda mais com a variável `\copyfitlines` ou `\copyfitmaxlines` comandos, que limitam o número de linhas que o algoritmo gerará. Ambos os comandos aceitam um parâmetro de contagem de linhas ou 0, para não limitar o número de linhas na região copiada.

`\copyfitlines` permite que o texto estouro para linhas adicionais se não se ajustar ao número especificado de linhas. Quebras explícitas de linha no segmento de texto que será copiado são sempre honradas.

`\copyfitmaxlines` sempre trunca linhas de saída extras que excedem o limite especificado. O número especificado de linhas nunca será excedido, mesmo se houver quebras de linha explícitas. Para esta versão do Image Serving, não mais do que N-1 `\line` os marcadores podem estar presentes na extensão de texto copiada. O comportamento será indefinido se esse limite for excedido.

## Exemplos {#section-f4ddbbfade444560be30a813d90c2c1b}

Os exemplos a seguir pressupõem que os corpos de texto são fornecidos com variáveis nomeadas *[!DNL $A$]*, *[!DNL $B$]* e *[!DNL $C$]*.

**Manter a mesma proporção entre tamanhos de fonte em todo o intervalo:**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* sempre será renderizado duas vezes maior que o restante do texto. Quando muito texto é especificado, *[!DNL $A$]* e *[!DNL $C$]* é renderizado com `\fs10` e *[!DNL $B$]* com `\fs20`. Com pouco texto, *[!DNL $A$]* e *[!DNL $C$]* usará `\fs100` e *[!DNL $B$]* `\fs200`.

**Converta em um tamanho de fonte grande comum se apenas uma pequena quantidade de texto for desenhada:**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

Na menor extremidade do intervalo, *[!DNL $B$]* é renderizado com `\fs20`, duas vezes maior que *[!DNL $A$]* e *[!DNL $C$]* at `\fs10`. Todo o texto é desenhado em `\fs100` (50 pts) na extremidade oposta do intervalo.

**Converta em um tamanho de fonte pequeno comum se houver muita quantidade de texto a ser renderizada:**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

Todo o texto é desenhado com \fs10 na extremidade pequena do intervalo, enquanto na maior, *[!DNL $A$]* e *[!DNL $C$]* são renderizados com `\fs100` e *[!DNL $B$]* com `\fs200`.

**Desative o ajuste de cópia para uma extensão de texto interna:**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

O tamanho da fonte para *[!DNL $A$]* e *[!DNL $C$]* pode variar entre 10 e 100, enquanto *[!DNL $B$]* é sempre renderizado com `\fs50`.

**Limitar a saída para uma única linha, mesmo se houver mais espaço vertical disponível, mas permitir que sobrefluxo para linhas adicionais se muito texto for especificado para caber em uma única linha em `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Limite a saída para uma única linha, mesmo se houver mais espaço vertical disponível. Se for especificado muito texto para caber em uma única linha em `\fs10` está truncado:**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
