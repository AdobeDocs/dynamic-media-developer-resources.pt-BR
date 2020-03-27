---
description: Permitir acesso direto a ativos baseados em caminho.
seo-description: Permitir acesso direto a ativos baseados em caminho.
seo-title: AllowDirectAccess
solution: Experience Manager
title: AllowDirectAccess
topic: Scene7 Image Serving - Image Rendering API
uuid: 6d413fac-6930-4f6d-90ad-62abb419efef
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AllowDirectAccess{#allowdirectaccess}

Permitir acesso direto a ativos baseados em caminho.

Quando esse atributo é definido, o acesso baseado em caminho é permitido ou restrito para os tipos de objetos especificados, dependendo se a palavra-chave `include` ou `exclude` é usada.

>[!NOTE]
>
>Se o `AllowDirectAccess` atributo não for especificado, o valor padrão será `exclude`.

* `include` permite o acesso aos tipos de objetos especificados e restringe o acesso de todos os outros.
* `exclude` restringe o acesso aos tipos de objetos especificados e permite o acesso de todos os outros.

Se nem `include` nem `exclude` for especificado, `include` é assumido.

Os seguintes tipos podem ser controlados:

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## Exemplos {#section-4c3765ebaa4245a799b454fc196f9237}

* Permitir acesso direto somente para tipos `IS` e `STATIC` objetos

   `AllowDirectAccess=include:IS,STATIC`

* Permitir acesso direto para todos os tipos de objetos, exceto `IS` e `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* Permitir acesso direto para *nenhum* tipo de objeto (ou seja, incluir nenhum)

   `AllowDirectAccess=include:`

* Permitir acesso direto para *todos* os tipos de objetos (ou seja, excluir nenhum)

   `AllowDirectAccess=exclude:`

* Equivalente a `include:IS,STATIC` (se `include`/ `exclude` não estiver presente, `include` é assumido)

   `AllowDirectAccess=IS,STATIC`

   Observe que esse é o valor padrão que é usado se o `AllowDirectAccess` atributo não for especificado para essa empresa.

* Incluir nenhum, equivalente a `include:` (se `include`/ `exclude` não estiver presente, `include` é assumido)

   `AllowDirectAccess=`

