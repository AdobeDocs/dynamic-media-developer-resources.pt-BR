---
description: Permitir acesso direto a ativos baseados em caminho.
solution: Experience Manager
title: PermitirAcessoDireto
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4000bdf-c21a-4976-82a7-70b2261dee0b
TQID: 'https://experienceleague.adobe.com/h2bcjdutPEZID471oI-MWfxG4trg87bIeyAxvoMyKEA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 166
ht-degree: 0%

---

# PermitirAcessoDireto{#allowdirectaccess}

Permitir acesso direto a ativos baseados em caminho.

Quando este atributo é definido, o acesso baseado em caminho é permitido ou restrito para os tipos de objeto especificados, dependendo se a palavra-chave `include` ou `exclude` é usada.

>[!NOTE]
>
>Se o atributo `AllowDirectAccess` não for especificado, o valor padrão será `exclude`.

* `include` permite o acesso aos tipos de objeto especificados e restringe o acesso a todos os outros.
* `exclude` restringe o acesso aos tipos de objeto especificados e permite o acesso a todos os outros.

Se `include` ou `exclude` não for especificado, `include` será presumido.

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

* Permitir acesso direto para *no* tipos de objeto (ou seja, não incluir)

  `AllowDirectAccess=include:`

* Permitir acesso direto a *todos* tipos de objetos (ou seja, excluir nenhum)

  `AllowDirectAccess=exclude:`

* Equivalente a `include:IS,STATIC` (se `include`/ `exclude` não estiver presente, `include` será presumido)

  `AllowDirectAccess=IS,STATIC`

  Observe que é o valor padrão que é usado se o atributo `AllowDirectAccess` não for especificado para esta empresa.

* Incluir nenhum, equivalente a `include:` (se `include`/ `exclude` não estiver presente, `include` será presumido)

  `AllowDirectAccess=`
