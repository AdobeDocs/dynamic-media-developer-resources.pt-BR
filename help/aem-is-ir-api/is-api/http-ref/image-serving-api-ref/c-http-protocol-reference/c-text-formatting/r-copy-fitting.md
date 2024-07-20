---
description: textPs= implementa um algoritmo proprietário de ajuste de cópia que ajusta automaticamente os tamanhos de fonte para preencher de forma ideal a área de texto com texto, minimizando o espaço extra na parte inferior e evitando o excesso.
solution: Experience Manager
title: Ajuste de cópia
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1a560f3-f92c-4143-b80a-e1674c8a4207
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# Ajuste de cópia{#copy-fitting}

textPs= implementa um algoritmo proprietário de ajuste de cópia que ajusta automaticamente os tamanhos de fonte para preencher de forma ideal a área de texto com texto, minimizando o espaço extra na parte inferior e evitando o excesso.

O ajuste de cópias pode ser ativado e controlado coletivamente para toda a camada de texto, em uma base de parágrafo, mesmo para uma extensão de texto individual.

Especifique o tamanho mínimo da fonte com `\fs` e o tamanho máximo da fonte com `\copyfit`. Qualquer número de intervalos é permitido na mesma cadeia de caracteres RTF. Os tamanhos de todos os intervalos variam proporcionalmente, garantindo que as taxas de tamanho de fonte desejadas sejam mantidas.

`\copyfit` é considerado um comando de formatação de caractere e tem regras de escopo como `\fs` e `\b`.

O ajuste de cópia está desabilitado ao especificar `\copyfit` com tamanho igual ou menor que o tamanho especificado com `\fs`.

## Limite de número de linhas {#section-e5aee0f039e04842afc3d6884ed681ac}

Além de especificar o intervalo de tamanhos de fonte, o comportamento do algoritmo de ajuste de cópia pode ser controlado ainda mais com os comandos `\copyfitlines` ou `\copyfitmaxlines`, que limitam o número de linhas geradas pelo algoritmo. Ambos os comandos aceitam um parâmetro de contagem de linhas ou 0, para não limitar o número de linhas na região copiada.

`\copyfitlines` permite que o texto estoure em linhas adicionais quando não couber no número de linhas especificado. Quebras de linha explícitas no segmento de texto a ser copiado são sempre honradas.

`\copyfitmaxlines` sempre trunca linhas de saída extras que excedem o limite especificado. O número de linhas especificado nunca é excedido, mesmo se houver quebras de linha explícitas. Nesta versão do Servidor de imagens, não podem estar presentes mais de N-1 marcadores `\line` na extensão de texto copiado. O comportamento será indefinido se esse limite for excedido.

## Exemplos {#section-f4ddbbfade444560be30a813d90c2c1b}

Os exemplos a seguir pressupõem que corpos de texto são fornecidos com variáveis chamadas *[!DNL $A$]*, *[!DNL $B$]* e *[!DNL $C$]*.

**Manter a mesma proporção entre os tamanhos de fonte em todo o intervalo:**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* é sempre renderizado com o dobro do tamanho do restante do texto. Quando muito texto é especificado, *[!DNL $A$]* e *[!DNL $C$]* é renderizado com `\fs10` e *[!DNL $B$]* com `\fs20`. Com pouco texto, *[!DNL $A$]* e *[!DNL $C$]* usam `\fs100` e *[!DNL $B$]* `\fs200`.

**Convergir para um tamanho de fonte grande comum se apenas uma pequena quantidade de texto for desenhada:**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

Na menor extremidade do intervalo, *[!DNL $B$]* é renderizado com `\fs20`, duas vezes maior que *[!DNL $A$]* e *[!DNL $C$]* em `\fs10`. Todo o texto é desenhado em `\fs100` (50 pontos) na extremidade oposta do intervalo.

**Convergir para um tamanho de fonte pequeno comum se houver muito texto a ser renderizado:**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

Todo o texto é desenhado com \fs10 na extremidade menor do intervalo, enquanto em sua maior, *[!DNL $A$]* e *[!DNL $C$]* são renderizados com `\fs100` e *[!DNL $B$]* com `\fs200`.

**Desabilitar ajuste de cópia para um intervalo de texto interno:**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

O tamanho da fonte de *[!DNL $A$]* e *[!DNL $C$]* pode variar entre 10 e 100, enquanto *[!DNL $B$]* é sempre renderizado com `\fs50`.

**Limitar a saída a uma única linha, mesmo que haja mais espaço vertical disponível, mas permitir que ela estoure em linhas adicionais se um texto em excesso for especificado para caber em uma única linha em `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Limitar a saída a uma única linha, mesmo se houver mais espaço vertical disponível. Se muito texto for especificado para caber em uma única linha em `\fs10`, ele será truncado:**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
