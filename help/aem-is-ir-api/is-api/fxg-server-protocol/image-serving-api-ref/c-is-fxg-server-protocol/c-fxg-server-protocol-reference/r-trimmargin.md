---
description: Defina a margem da aparação. Define a margem de corte que é definida no arquivo PDF.
seo-description: Defina a margem da aparação. Define a margem de corte que é definida no arquivo PDF.
seo-title: trimMargin
solution: Experience Manager
title: trimMargin
uuid: af94f9e8-a32e-439a-817a-a40aa8dc7dd4
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---


# trimMargin{#trimmargin}

Defina a margem da aparação. Define a margem de corte que é definida no arquivo PDF.

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` em pontos

Por padrão, `trimMargin` é definido no tamanho total do documento definido por `viewWidth` e `viewHeight`. Os valores *[!DNL left]*, *[!DNL bottom]* e *[!DNL right]* são padronizados para o valor *[!DNL top]* se não for especificado.
