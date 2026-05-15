---
title: Exemplos
description: Este exemplo usa o Servidor de imagens para colorir um objeto e aplicar um decalque contendo texto personalizado em um de um conjunto de vinhetas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
TQID: 'https://experienceleague.adobe.com/GMzKDuP-wzTrPJQbxpXc0M08BjCQdWCkGo5jOUiWipU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 137
ht-degree: 0%

---

# Exemplos{#examples}

Este exemplo usa o Servidor de imagens para colorir um objeto e aplicar um decalque contendo texto personalizado em um de um conjunto de vinhetas.

As variáveis IR são usadas para identificar a vinheta, a imagem do logotipo e o texto personalizado.

O campo `vignette::Modifier` no registro denominado *modelo* no mapa de vinheta do catálogo de materiais `myCat` contém o seguinte:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Todas as vinhetas usadas estão listadas no mapa de vinhetas do catálogo de materiais `myCat`.

O cliente agora pode fazer a seguinte solicitação para recuperar a imagem padrão (usa as variáveis definidas no início do modelo):

[!DNL `https://server/myCat/template`]

A solicitação a seguir especifica determinado conteúdo a ser renderizado:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Consulte a Documentação do Servidor de Imagens para obter detalhes sobre o comando Servidor de Imagens `text=`.
