---
title: Exemplos
description: Este exemplo usa o Servidor de imagens para colorir um objeto e aplicar um decalque contendo texto personalizado em um de um conjunto de vinhetas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Exemplos{#examples}

Este exemplo usa o Servidor de imagens para colorir um objeto e aplicar um decalque contendo texto personalizado em um de um conjunto de vinhetas.

As variáveis IR são usadas para identificar a vinheta, a imagem do logotipo e o texto personalizado.

A variável `vignette::Modifier` campo no registro chamado *modelo* no mapa de vinheta do catálogo de materiais `myCat` contém o seguinte:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Todas as vinhetas usadas estão listadas no mapa de vinhetas do catálogo de materiais `myCat`.

O cliente agora pode fazer a seguinte solicitação para recuperar a imagem padrão (usa as variáveis definidas no início do modelo):

[!DNL `https://server/myCat/template`]

A solicitação a seguir especifica determinado conteúdo a ser renderizado:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Consulte a Documentação do Servidor de imagens para obter detalhes sobre esse serviço `text=` comando.
