---
title: Catálogos de materiais
description: Catálogos de materiais oferecem várias características.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 502f80f5-fdd1-468b-89a9-64cc9128d655
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Catálogos de materiais {#material-catalogs}

Catálogos de materiais oferecem várias características.

* Permitir definição persistente de materiais, incluindo todas as propriedades do material.

  Os materiais definidos no catálogo de materiais podem ser referenciados usando uma ID simples, em vez de um conjunto de propriedades do material.
* Forneça padrões para determinados atributos de solicitação, como a qualidade do JPEG ou o tamanho padrão da imagem de resposta.
* Gerencie vinhetas, perfis ICC e modelos de solicitação.

Mesmo que nenhum catálogo de materiais específico seja definido, todos os recursos dos catálogos de materiais estarão disponíveis no catálogo padrão ( [!DNL default.ini]).

Embora os materiais de renderização possam ser especificados explicitamente em solicitações usando atributos de material, geralmente é mais desejável ocultar os detalhes dos materiais do site usando catálogos de materiais. src= comandos aceitam referências de catálogo em vez de caminhos de arquivo explícitos. Uma entrada de catálogo consiste em ` [ *[!DNL catId]*/] *[!DNL itemId]*`, onde ` *[!DNL catId]*` identifica um catálogo de materiais e ` *[!DNL itemId]*` identifica um registro no catálogo. Se ` *[!DNL catId]*` não for especificado, o catálogo da sessão será usado (veja abaixo).

Um registro de catálogo será correspondido com êxito se (a) ` *[!DNL catId]*` corresponder ao valor `attribute::RootId` de um catálogo de materiais e (b) ` *[!DNL recId]*` corresponder ao valor catalog::Id no mesmo catálogo. Se houver uma correspondência bem-sucedida, os atributos do material (incluindo `src=`) serão definidos para os dados do registro do catálogo. Se o MSS incluir atributos adicionais para esse material além de src=, eles substituirão os valores do registro do catálogo.

Se ` *[!DNL recId]*` não for compatível com uma entrada de catálogo, ` *[!DNL catId]*` será substituído por `attribute::RootPath` do catálogo e o caminho resultante será considerado um caminho de arquivo simples. Outros atributos padrão (por exemplo, `attribute::Resolution`) também podem ser herdados do catálogo de materiais.

As vinhetas e os perfis de ICC podem ser discriminados em catálogos de materiais semelhantes aos próprios materiais e com propriedades dadas. Além disso, o mapa de vinheta também fornece o contêiner de modelos.

**Consulte também**

Referência do Catálogo de Materiais, [`src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
