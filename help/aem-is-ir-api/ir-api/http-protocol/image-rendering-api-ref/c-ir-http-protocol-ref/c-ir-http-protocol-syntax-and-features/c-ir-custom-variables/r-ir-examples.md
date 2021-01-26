---
description: Este exemplo usa o Serviço de imagem para colorir um objeto e aplicar uma declaração que contém texto personalizado em um dos conjuntos de vinhetas.
seo-description: Este exemplo usa o Serviço de imagem para colorir um objeto e aplicar uma declaração que contém texto personalizado em um dos conjuntos de vinhetas.
seo-title: Exemplos
solution: Experience Manager
title: Exemplos
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9f8e4346-6efe-4f21-982d-613328bd708d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---


# Exemplos{#examples}

Este exemplo usa o Serviço de imagem para colorir um objeto e aplicar uma declaração que contém texto personalizado em um dos conjuntos de vinhetas.

As variáveis IR são usadas para identificar a vinheta, a imagem do logotipo e o texto personalizado.

O campo `vignette::Modifier` no registro chamado *template* no mapa de vinheta do catálogo de materiais `myCat` contém o seguinte:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Todas as vinhetas que serão usadas estão listadas no mapa de vinheta do catálogo de materiais `myCat`.

O cliente agora pode fazer a seguinte solicitação para recuperar a imagem padrão (isso usa as variáveis definidas no início do modelo):

[!DNL `https://server/myCat/template`]

A solicitação a seguir especifica determinado conteúdo a ser renderizado:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Consulte a Documentação de disponibilização de imagem para obter detalhes sobre o comando de disponibilização de imagem `text=`.
