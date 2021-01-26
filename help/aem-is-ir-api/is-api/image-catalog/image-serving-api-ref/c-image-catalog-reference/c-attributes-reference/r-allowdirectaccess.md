---
description: Permitir acesso direto a ativos baseados em caminho.
seo-description: Permitir acesso direto a ativos baseados em caminho.
seo-title: AllowDirectAccess
solution: Experience Manager
title: AllowDirectAccess
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6d413fac-6930-4f6d-90ad-62abb419efef
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---


# AllowDirectAccess{#allowdirectaccess}

Permitir acesso direto a ativos baseados em caminho.

Quando esse atributo é definido, o acesso baseado em caminho é permitido ou restrito para os tipos de objetos especificados, dependendo se a palavra-chave `include` ou `exclude` é usada.

>[!NOTE]
>
>Se o atributo `AllowDirectAccess` não for especificado, o valor padrão será `exclude`.

* `include` permite o acesso aos tipos de objetos especificados e restringe o acesso de todos os outros.
* `exclude` restringe o acesso aos tipos de objetos especificados e permite o acesso de todos os outros.

Se `include` ou `exclude` não for especificado, `include` será assumido.

Os seguintes tipos podem ser controlados:

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## Exemplos {#section-4c3765ebaa4245a799b454fc196f9237}

* Permitir acesso direto somente para os tipos de objetos `IS` e `STATIC`

   `AllowDirectAccess=include:IS,STATIC`

* Permitir acesso direto para todos os tipos de objetos, exceto `IS` e `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* Permitir acesso direto para tipos de objetos *no* (ou seja, incluir nenhum)

   `AllowDirectAccess=include:`

* Permitir acesso direto para os tipos de objetos *all* (ou seja, excluir nenhum)

   `AllowDirectAccess=exclude:`

* Equivalente a `include:IS,STATIC` (se `include`/ `exclude` não estiver presente, `include` será assumido)

   `AllowDirectAccess=IS,STATIC`

   Observe que esse é o valor padrão que é usado se o atributo `AllowDirectAccess` não for especificado para essa empresa.

* Incluir nenhum, equivalente a `include:` (se `include`/ `exclude` não estiver presente, `include` será assumido)

   `AllowDirectAccess=`

