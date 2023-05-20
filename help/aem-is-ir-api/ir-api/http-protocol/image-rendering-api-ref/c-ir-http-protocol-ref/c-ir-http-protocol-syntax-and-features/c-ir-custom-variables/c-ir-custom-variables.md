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

`[!DNL name]` - Nome da variável. Pode consistir em qualquer combinação de caracteres alfabéticos, dígitos e seguros, excluindo `$`.

`[!DNL value]` - Valor com o qual a variável deve ser definida (string).

As variáveis são definidas de forma semelhante a outros comandos do servidor, usando a sintaxe acima. As variáveis devem ser definidas antes de serem referenciadas. Variáveis definidas em `vignette::Modifier` podem ser referenciados na solicitação de URL e vice-versa.

>[!NOTE]
>
>`[!DNL value]` deve ser codificado em URL de passagem única para transmissão HTTP segura. A codificação dupla é necessária se `[!DNL value]` O é retransmitido por meio de HTTP. Esta situação ocorre quando `[!DNL value]` é substituída em uma solicitação externa aninhada.

As variáveis são referenciadas incorporando o nome da variável (delimitado por uma à esquerda e uma à direita) `$`) em qualquer lugar nos valores de comando. Por exemplo, entre a variável `=`  seguindo o nome do comando e as configurações subsequentes `&` ou no final da solicitação. O servidor substitui cada ocorrência de `$ [!DNL name]$` com `[!DNL string]`. Não ocorrem substituições em nenhuma ocorrência de `$ [!DNL name]$` em nomes de comando (antes do sinal de igual de um comando) e na parte do caminho da solicitação.

As variáveis personalizadas não podem ser aninhadas. Qualquer ocorrência de `$ [!DNL name]$` no prazo de `[!DNL string]` não são substituídas. Por exemplo, o fragmento de solicitação `$var2=apple&$var1=my$var2$tree&text=$var1$` resolve para `text=my$var2$tree`.

`$` não é um caractere reservado; pode ocorrer de outra forma na solicitação. Por exemplo, `src=my$texture$file.tif` é um comando válido (supondo que uma entrada de catálogo de material ou arquivo de textura chamado `[!DNL my$texture$file.tif]` existe), enquanto `wid=$number$` não é, porque `wid=` requer um argumento numérico.
