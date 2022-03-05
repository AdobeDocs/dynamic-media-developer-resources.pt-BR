---
title: Variáveis personalizadas
description: A parte de consulta de solicitações e cadeias de caracteres do modificador de vinheta pode incluir variáveis definidas pelo usuário.
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

A parte de consulta de solicitações e cadeias de caracteres vinheta::modificador pode incluir variáveis definidas pelo usuário.

`$ [!DNL name] = [!DNL value]`

`[!DNL name]` - Nome da variável. Pode consistir em qualquer combinação de caracteres alfa, dígito e seguros, excluindo `$`.

`[!DNL value]` - Valor ao qual a variável deve ser definida (string).

As variáveis são definidas de forma semelhante a outros comandos do servidor, usando a sintaxe acima. As variáveis devem ser definidas antes de serem referenciadas. Variáveis definidas em `vignette::Modifier` pode ser referenciado na solicitação de URL e, inversamente.

>[!NOTE]
>
>`[!DNL value]` deve ser codificado por URL de passagem única para transmissão HTTP segura. Codificação dupla é necessária se `[!DNL value]` é retransmitido por meio de HTTP. Esta situação ocorre quando `[!DNL value]` é substituída em uma solicitação externa aninhada.

As variáveis são referenciadas com a incorporação do nome da variável (delimitado por um à esquerda e um à direita) `$`) em qualquer lugar nos valores do comando. Por exemplo, entre as `=`  seguindo o nome do comando e o seguinte `&` ou o fim da solicitação. O servidor substitui cada ocorrência de `$ [!DNL name]$` com `[!DNL string]`. Não há substituições em nenhuma ocorrência de `$ [!DNL name]$` em nomes de comando (antes do sinal de igual de um comando) e na parte do caminho da solicitação.

As variáveis personalizadas podem não estar aninhadas. Quaisquer ocorrências de `$ [!DNL name]$` within `[!DNL string]` não são substituídas. Por exemplo, o fragmento de solicitação `$var2=apple&$var1=my$var2$tree&text=$var1$` resolve `text=my$var2$tree`.

`$` não é um caráter reservado; pode ocorrer de outra forma na solicitação. Por exemplo, `src=my$texture$file.tif` é um comando válido (supondo que uma entrada de catálogo de material ou arquivo de textura chamado `[!DNL my$texture$file.tif]` existe), while `wid=$number$` não, porque `wid=` exige um argumento numérico.
