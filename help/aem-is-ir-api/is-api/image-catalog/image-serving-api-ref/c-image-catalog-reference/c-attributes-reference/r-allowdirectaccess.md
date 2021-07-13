---
description: Permitir acesso direto a ativos baseados em caminho.
solution: Experience Manager
title: AllowDirectAccess
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# AllowDirectAccess{#allowdirectaccess}

Permitir acesso direto a ativos baseados em caminho.

Quando este atributo é definido, o acesso baseado em caminho é permitido ou restrito para os tipos de objeto especificados, dependendo se a palavra-chave `include` ou `exclude` é usada.

>[!NOTE]
>
>Se o atributo `AllowDirectAccess` não for especificado, o valor padrão será `exclude`.

* `include` permite o acesso para os tipos de objetos especificados e restringe o acesso para todos os outros.
* `exclude` restringe o acesso dos tipos de objetos especificados e permite o acesso de todos os outros.

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

* Permitir acesso direto apenas para os tipos de objetos `IS` e `STATIC`

   `AllowDirectAccess=include:IS,STATIC`

* Permitir acesso direto para todos os tipos de objetos, exceto `IS` e `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* Permitir acesso direto para tipos de objetos *no* (ou seja, não incluir nenhum)

   `AllowDirectAccess=include:`

* Permitir acesso direto para os tipos de objetos *all* (ou seja, excluir nenhum)

   `AllowDirectAccess=exclude:`

* Equivalente a `include:IS,STATIC` (se `include`/ `exclude` não estiver presente, `include` será assumido)

   `AllowDirectAccess=IS,STATIC`

   Observe que é o valor padrão usado se o atributo `AllowDirectAccess` não for especificado para essa empresa.

* Inclua nenhum, equivalente a `include:` (se `include`/ `exclude` não estiver presente, `include` será considerado)

   `AllowDirectAccess=`
