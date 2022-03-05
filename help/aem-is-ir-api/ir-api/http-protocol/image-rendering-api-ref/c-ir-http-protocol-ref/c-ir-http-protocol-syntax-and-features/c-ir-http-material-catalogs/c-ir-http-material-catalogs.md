---
title: Catálogos de materiais
description: Os catálogos de materiais oferecem vários recursos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 502f80f5-fdd1-468b-89a9-64cc9128d655
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Catálogos de materiais {#material-catalogs}

Os catálogos de materiais oferecem vários recursos.

* Permitir a definição persistente de materiais, incluindo todas as propriedades dos materiais.

   Os materiais definidos no catálogo de materiais podem ser referenciados usando uma ID simples, em vez de um conjunto de propriedades de material.
* Forneça padrões para determinados atributos de solicitação, como a qualidade da JPEG ou um tamanho de imagem de resposta padrão.
* Gerencie vinhetas, perfis ICC e modelos de solicitação.

Mesmo que não sejam definidos catálogos de materiais específicos, todos os recursos de catálogos de materiais estão disponíveis através do catálogo padrão ( [!DNL default.ini]).

Embora os materiais de renderização possam ser especificados explicitamente em solicitações usando atributos de material, geralmente é mais desejável ocultar os detalhes dos materiais do site usando catálogos de material. os comandos src= aceitam referências de catálogo em vez de caminhos de arquivo explícitos. Uma entrada de catálogo consiste em ` [ *[!DNL catId]*/] *[!DNL itemId]*`, onde ` *[!DNL catId]*` identifica um catálogo de materiais e ` *[!DNL itemId]*` identifica um registro no catálogo. If ` *[!DNL catId]*` não for especificado, o catálogo de sessão será usado (veja abaixo).

Um registro de catálogo é correspondido com êxito se (a) ` *[!DNL catId]*` corresponde ao `attribute::RootId` valor de um catálogo de materiais e b) ` *[!DNL recId]*` corresponde ao valor catalog::Id no mesmo catálogo. Se houver uma correspondência bem-sucedida, os atributos do material (incluindo `src=`) são definidas para os dados do registro do catálogo. Se o MSS incluir atributos adicionais para esse material além de src=, eles substituirão os valores do registro do catálogo.

If ` *[!DNL recId]*` não pode corresponder a uma entrada de catálogo, ` *[!DNL catId]*` é substituído por `attribute::RootPath` do catálogo e o caminho resultante é então considerado um caminho de arquivo simples. Outros atributos padrão (por exemplo, `attribute::Resolution`) também pode ser herdada do catálogo de materiais.

Vinhetas e perfis ICC podem ser discriminados em catálogos de materiais semelhantes aos próprios materiais e propriedades específicas. Além disso, o mapa de vinheta também fornece o contêiner para modelos.

**Consulte também**

Referência do catálogo de materiais, [ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
