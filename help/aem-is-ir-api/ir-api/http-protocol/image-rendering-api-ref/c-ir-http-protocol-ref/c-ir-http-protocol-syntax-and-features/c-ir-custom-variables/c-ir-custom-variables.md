---
description: A parte do query das solicitações e das sequências de caracteres do modificador de vinheta pode incluir variáveis definidas pelo usuário.
seo-description: A parte do query das solicitações e das sequências de caracteres do modificador de vinheta pode incluir variáveis definidas pelo usuário.
seo-title: Variáveis personalizadas
solution: Experience Manager
title: Variáveis personalizadas
topic: Scene7 Image Serving - Image Rendering API
uuid: 933fba00-759c-4bd3-bada-eec751426d9e
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---


# Variáveis personalizadas{#custom-variables}

A parte do query das solicitações e as sequências de caracteres de vinheta::Modifier podem incluir variáveis definidas pelo usuário.

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **Nome da variável. Pode consistir em qualquer combinação de caracteres alfa, dígito e seguros, excluindo &#39;$&#39;.

** *[!DNL value]* ** Valor ao qual a variável deve ser definida (string).

As variáveis são definidas de forma semelhante a outros comandos do servidor, usando a sintaxe acima. As variáveis devem ser definidas antes que possam ser referenciadas. As variáveis definidas em `vignette::Modifier` podem ser referenciadas na solicitação de URL e vice-versa.

>[!NOTE]
>
>*[!DNL value]* deve ser codificado em URL de passagem única para transmissão segura HTTP. A codificação do Duplo é necessária se *[!DNL value]* for retransmitida via HTTP. Esse é o caso quando *[!DNL value]* é substituído em uma solicitação estrangeira aninhada.

As variáveis são referenciadas pela incorporação do nome da variável (delimitado por um $ à esquerda e um $ à direita) em qualquer lugar nos valores de comando. Por exemplo, entre &#39;=&#39; após o nome do comando e o &#39;&amp;&#39; subsequente ou o fim da solicitação. O servidor substitui cada ocorrência de $ *[!DNL name]*$ por *[!DNL string]*. Nenhuma substituição ocorrerá em nenhuma ocorrência de $ *[!DNL name]*$ em nomes de comando (antes do sinal de igual de um comando) e na parte do caminho da solicitação.

As variáveis personalizadas não podem ser aninhadas. Nenhuma ocorrência de $ *[!DNL name]*$ dentro *[!DNL string]* é substituída. Por exemplo, o fragmento de solicitação `$var2=apple&$var1=my$var2$tree&text=$var1$` é resolvido como `text=my$var2$tree`.

$ não é um caractere reservado; pode ocorrer de outra forma na solicitação. Por exemplo, `src=my$texture$file.tif` é um comando válido (assumindo que uma entrada de catálogo de material ou um arquivo de textura chamado [!DNL my$texture$file.tif] existe), enquanto `wid=$number$` não é, porque `wid=` requer um argumento numérico.
