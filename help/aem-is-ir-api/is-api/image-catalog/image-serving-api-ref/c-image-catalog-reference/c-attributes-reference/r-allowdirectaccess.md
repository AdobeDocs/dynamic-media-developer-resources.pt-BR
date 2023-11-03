---
description: Permitir acesso direto a ativos baseados em caminho.
solution: Experience Manager
title: PermitirAcessoDireto
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# PermitirAcessoDireto{#allowdirectaccess}

Permitir acesso direto a ativos baseados em caminho.

Quando este atributo é definido, o acesso baseado em caminho é permitido ou restrito para os tipos de objeto especificados, dependendo se a variável `include` ou `exclude` palavra-chave é usada.

>[!NOTE]
>
>Se a variável `AllowDirectAccess` atributo não for especificado, o valor padrão será `exclude`.

* `include` permite o acesso aos tipos de objeto especificados e restringe o acesso a todos os outros.
* `exclude` restringe o acesso aos tipos de objeto especificados e permite o acesso a todos os outros.

Se nenhuma delas `include` nem `exclude` é especificado, `include` é presumido.

Os seguintes tipos podem ser controlados:

* `SVG`
* `IS`
* `STATIC`
* `FXG`
* `FLA`
* `IR_VNT`
* `IR_MAT`

## Exemplos {#section-4c3765ebaa4245a799b454fc196f9237}

* Permitir acesso direto apenas para `IS` e `STATIC` tipos de objeto

  `AllowDirectAccess=include:IS,STATIC`

* Permitir acesso direto para todos os tipos de objetos, exceto `IS` e `STATIC``AllowDirectAccess=exclude:IS,STATIC`

* Permitir acesso direto a *não* tipos de objeto (ou seja, não incluir)

  `AllowDirectAccess=include:`

* Permitir acesso direto a *all* tipos de objeto (ou seja, excluir nenhum)

  `AllowDirectAccess=exclude:`

* Equivalente a `include:IS,STATIC` (se `include`/ `exclude` não está presente, `include` é presumido)

  `AllowDirectAccess=IS,STATIC`

  Observe que é o valor padrão usado se a variável `AllowDirectAccess` o atributo não foi especificado para esta empresa.

* Incluir nenhum, equivalente a `include:` (se `include`/ `exclude` não está presente, `include` é presumido)

  `AllowDirectAccess=`
