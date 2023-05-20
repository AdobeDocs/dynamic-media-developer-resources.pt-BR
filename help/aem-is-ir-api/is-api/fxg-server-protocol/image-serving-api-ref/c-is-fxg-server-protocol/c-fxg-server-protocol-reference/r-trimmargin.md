---
description: Definir margem de corte. Define a margem de apara definida no arquivo PDF.
solution: Experience Manager
title: trimMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc6e31f8-d3be-44d3-8342-a4ef4b3fd61b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# trimMargin{#trimmargin}

Definir margem de corte. Define a margem de apara definida no arquivo PDF.

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` nos pontos

Por padrão, a variável `trimMargin` está definido com o tamanho máximo do documento definido por `viewWidth` e `viewHeight`. A variável *[!DNL left]*, *[!DNL bottom]*, e *[!DNL right]* os valores são padronizados para o *[!DNL top]* valor, se não for especificado.
