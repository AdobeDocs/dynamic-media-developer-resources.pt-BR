---
description: Catálogos de materiais ofertas com vários recursos.
seo-description: Catálogos de materiais ofertas com vários recursos.
seo-title: Catálogos de materiais *
solution: Experience Manager
title: Catálogos de materiais *
topic: Scene7 Image Serving - Image Rendering API
uuid: 2a2f371e-0982-47c7-b3da-678a5ff6c7a7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---


# Catálogos de materiais *{#material-catalogs}

Catálogos de materiais ofertas com vários recursos.

* Permitir a definição persistente de materiais, incluindo todas as propriedades de materiais.

   Os materiais definidos no catálogo de materiais podem ser referenciados usando uma ID simples, em vez de um conjunto de propriedades de material.
* Forneça padrões para determinados atributos de solicitação, como a qualidade JPEG ou um tamanho de imagem de resposta padrão.
* Gerencie vinhetas, perfis ICC e modelos de solicitação.

Mesmo se nenhum catálogo de materiais específico for definido, todos os recursos de catálogos de materiais estarão disponíveis por meio do catálogo padrão ( [!DNL default.ini]).

Embora os materiais de renderização possam ser especificados explicitamente em solicitações usando atributos de material, em muitos casos é mais desejável ocultar os detalhes dos materiais do site usando catálogos de materiais. os comandos src= aceitam referências de catálogo em vez de caminhos de arquivo explícitos. Uma entrada de catálogo consiste em ` [ *[!DNL catId]*/] *[!DNL itemId]*`, onde ` *[!DNL catId]*` identifica um catálogo de materiais e ` *[!DNL itemId]*` identifica um registro no catálogo. Se ` *[!DNL catId]*` não for especificado, o catálogo de sessões será usado (consulte abaixo).

Uma correspondência de registro de catálogo terá êxito se (a) ` *[!DNL catId]*` corresponder ao valor `attribute::RootId` de um catálogo de materiais e (b) ` *[!DNL recId]*` corresponder ao valor do catálogo::Id no mesmo catálogo. No caso de uma correspondência bem-sucedida, os atributos do material (incluindo `src=`) são definidos para os dados do registro do catálogo. Se o MSS incluir atributos adicionais para esse material além de src=, eles substituirão os valores do registro do catálogo.

Se ` *[!DNL recId]*` não puder ser correspondido a uma entrada de catálogo, ` *[!DNL catId]*` será substituído por `attribute::RootPath` do catálogo e o caminho resultante será considerado um caminho de arquivo simples. Outros atributos padrão (por exemplo, `attribute::Resolution`) também pode ser herdado do catálogo de materiais.

As vinhetas e os perfis ICC podem ser discriminados em catálogos de materiais semelhantes aos próprios materiais e a determinadas propriedades. Além disso, o mapa de vinheta também fornece o container para modelos.

**Consulte também**

Referência do catálogo de materiais, [ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
