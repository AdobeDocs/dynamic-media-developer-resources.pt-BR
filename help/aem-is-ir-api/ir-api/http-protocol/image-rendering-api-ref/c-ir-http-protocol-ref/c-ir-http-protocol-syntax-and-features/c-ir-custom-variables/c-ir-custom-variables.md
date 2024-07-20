---
title: Variáveis personalizadas
description: A parte de consulta das solicitações e as cadeias de caracteres do Modificador de vinheta podem incluir variáveis definidas pelo usuário.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8d26b797-5099-49fb-b7e0-46747f35ab84
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---

# Variáveis personalizadas{#custom-variables}

A parte de consulta das solicitações e as strings vignette::Modifier podem incluir variáveis definidas pelo usuário.

`$ [!DNL name] = [!DNL value]`

`[!DNL name]` - Nome da variável. Pode consistir em qualquer combinação de caracteres alfabéticos, dígitos e seguros, exceto `$`.

`[!DNL value]` - Valor para o qual a variável deve ser definida (cadeia de caracteres).

As variáveis são definidas de forma semelhante a outros comandos do servidor, usando a sintaxe acima. As variáveis devem ser definidas antes de serem referenciadas. As variáveis definidas em `vignette::Modifier` podem ser referenciadas na solicitação de URL e vice-versa.

>[!NOTE]
>
>`[!DNL value]` deve ser codificado em URL de passagem única para transmissão HTTP segura. A codificação dupla será necessária se `[!DNL value]` for retransmitido por meio de HTTP. Esta situação ocorre quando `[!DNL value]` é substituído em uma solicitação externa aninhada.

As variáveis são referenciadas incorporando o nome da variável (delimitado por um `$` à esquerda e à direita) em qualquer lugar nos valores do comando. Por exemplo, entre o `=` que segue o nome do comando e o `&` subsequente ou o fim da solicitação. O servidor substitui cada ocorrência de `$ [!DNL name]$` por `[!DNL string]`. Não ocorrem substituições em nenhuma ocorrência de `$ [!DNL name]$` em nomes de comando (antes do sinal de igual de um comando) e na parte do caminho da solicitação.

As variáveis personalizadas não podem ser aninhadas. Nenhuma ocorrência de `$ [!DNL name]$` em `[!DNL string]` é substituída. Por exemplo, o fragmento de solicitação `$var2=apple&$var1=my$var2$tree&text=$var1$` é resolvido como `text=my$var2$tree`.

`$` não é um caractere reservado; caso contrário, pode ocorrer na solicitação. Por exemplo, `src=my$texture$file.tif` é um comando válido (supondo que exista uma entrada de catálogo de material ou arquivo de textura chamado `[!DNL my$texture$file.tif]`), enquanto `wid=$number$` não é, porque `wid=` requer um argumento numérico.
