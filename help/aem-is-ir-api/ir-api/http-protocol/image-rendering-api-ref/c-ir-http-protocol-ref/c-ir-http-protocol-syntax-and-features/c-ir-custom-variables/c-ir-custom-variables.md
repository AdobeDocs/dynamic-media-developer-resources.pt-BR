---
description: A parte de consulta de solicitações e cadeias de caracteres do modificador de vinheta pode incluir variáveis definidas pelo usuário.
seo-description: A parte de consulta de solicitações e cadeias de caracteres do modificador de vinheta pode incluir variáveis definidas pelo usuário.
seo-title: Variáveis personalizadas
solution: Experience Manager
title: Variáveis personalizadas
uuid: 933fba00-759c-4bd3-bada-eec751426d9e
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---


# Variáveis personalizadas{#custom-variables}

A parte de consulta de solicitações e cadeias de caracteres vinheta::modificador pode incluir variáveis definidas pelo usuário.

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **Nome da variável. Pode consistir em qualquer combinação de caracteres alfa, dígito e seguros, excluindo &#39;$&#39;.

** *[!DNL value]* ** Valor ao qual a variável deve ser definida (cadeia de caracteres).

As variáveis são definidas de forma semelhante a outros comandos do servidor, usando a sintaxe acima. As variáveis devem ser definidas antes de serem referenciadas. As variáveis definidas em `vignette::Modifier` podem ser referenciadas na solicitação de URL, e vice-versa.

>[!NOTE]
>
>*[!DNL value]* deve ser codificado por URL de passagem única para transmissão HTTP segura. É necessária codificação dupla se *[!DNL value]* for retransmitido via HTTP. Esse é o caso quando *[!DNL value]* é substituído em uma solicitação externa aninhada.

As variáveis são referenciadas incorporando o nome da variável (delimitado por um $ à esquerda e um $ à direita) em qualquer lugar nos valores do comando. Por exemplo, entre o &#39;=&#39; após o nome do comando e o &#39;&amp;&#39; subsequente ou o fim da solicitação. O servidor substitui cada ocorrência de $ *[!DNL name]*$ por *[!DNL string]*. Nenhuma substituição ocorrerá em qualquer ocorrência de $ *[!DNL name]*$ em nomes de comando (antes do sinal de igual de um comando) e na parte do caminho da solicitação.

As variáveis personalizadas podem não estar aninhadas. Quaisquer ocorrências de $ *[!DNL name]*$ em *[!DNL string]* não são substituídas. Por exemplo, o fragmento de solicitação `$var2=apple&$var1=my$var2$tree&text=$var1$` resolve para `text=my$var2$tree`.

$ não é um caractere reservado; pode ocorrer de outra forma na solicitação. Por exemplo, `src=my$texture$file.tif` é um comando válido (assumindo que existe uma entrada de catálogo de materiais ou um arquivo de textura chamado [!DNL my$texture$file.tif]), enquanto `wid=$number$` não é, porque `wid=` requer um argumento numérico.
