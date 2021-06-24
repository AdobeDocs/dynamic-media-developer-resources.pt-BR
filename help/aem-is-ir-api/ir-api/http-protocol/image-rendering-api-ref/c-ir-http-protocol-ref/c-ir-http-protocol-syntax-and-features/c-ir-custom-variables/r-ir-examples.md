---
description: Este exemplo usa o Serviço de imagem para colorir um objeto e aplicar um decalque contendo texto personalizado em uma de um conjunto de vinhetas.
solution: Experience Manager
title: Exemplos
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# Exemplos{#examples}

Este exemplo usa o Serviço de imagem para colorir um objeto e aplicar um decalque contendo texto personalizado em uma de um conjunto de vinhetas.

As variáveis IR são usadas para identificar a vinheta, a imagem do logotipo e o texto personalizado.

O campo `vignette::Modifier` no registro chamado *template* no mapa de vinheta do catálogo de materiais `myCat` contém o seguinte:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Todas as vinhetas que serão usadas são listadas no mapa de vinheta do catálogo de materiais `myCat`.

O cliente agora pode fazer a seguinte solicitação para recuperar a imagem padrão (isso usa as variáveis definidas no início do template):

[!DNL `https://server/myCat/template`]

A solicitação a seguir especifica o conteúdo a ser renderizado:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Consulte a Documentação de disponibilização de imagens para obter detalhes sobre o comando de disponibilização de imagens `text=`.
