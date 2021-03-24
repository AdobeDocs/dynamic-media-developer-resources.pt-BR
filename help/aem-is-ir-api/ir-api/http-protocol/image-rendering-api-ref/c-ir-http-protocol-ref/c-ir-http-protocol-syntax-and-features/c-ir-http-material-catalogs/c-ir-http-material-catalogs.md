---
description: Os catálogos de materiais oferecem vários recursos.
solution: Experience Manager
title: Catálogos de materiais *
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---


# Catálogos de materiais *{#material-catalogs}

Os catálogos de materiais oferecem vários recursos.

* Permitir a definição persistente de materiais, incluindo todas as propriedades dos materiais.

   Os materiais definidos no catálogo de materiais podem ser referenciados usando uma ID simples, em vez de um conjunto de propriedades de material.
* Forneça padrões para determinados atributos de solicitação, como a qualidade JPEG ou um tamanho de imagem de resposta padrão.
* Gerencie vinhetas, perfis ICC e modelos de solicitação.

Mesmo que não sejam definidos catálogos de materiais específicos, todos os recursos de catálogos de materiais estão disponíveis através do catálogo padrão ( [!DNL default.ini]).

Embora os materiais de renderização possam ser especificados explicitamente em solicitações usando atributos de material, em muitos casos, é mais desejável ocultar os detalhes dos materiais no site usando catálogos de material. os comandos src= aceitam referências de catálogo em vez de caminhos de arquivo explícitos. Uma entrada de catálogo consiste em ` [ *[!DNL catId]*/] *[!DNL itemId]*`, onde ` *[!DNL catId]*` identifica um catálogo de materiais e ` *[!DNL itemId]*` identifica um registro no catálogo. Se ` *[!DNL catId]*` não for especificado, o catálogo de sessão será usado (veja abaixo).

Um registro de catálogo é correspondido com êxito se (a) ` *[!DNL catId]*` corresponder ao valor `attribute::RootId` de um catálogo de materiais e (b) ` *[!DNL recId]*` corresponder ao valor catalog::Id no mesmo catálogo. No caso de uma correspondência bem-sucedida, os atributos do material (incluindo `src=`) são definidos para os dados do registro do catálogo. Se o MSS incluir atributos adicionais para esse material além de src=, eles substituirão os valores do registro do catálogo.

Se ` *[!DNL recId]*` não puder ser correspondido a uma entrada de catálogo, ` *[!DNL catId]*` será substituído por `attribute::RootPath` do catálogo e o caminho resultante será considerado um caminho de arquivo simples. Outros atributos padrão (por exemplo, `attribute::Resolution`) também pode ser herdada do catálogo de materiais.

Vinhetas e perfis ICC podem ser discriminados em catálogos de materiais semelhantes aos próprios materiais e propriedades específicas. Além disso, o mapa de vinheta também fornece o contêiner para modelos.

**Consulte também**

Referência do catálogo de materiais, [ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
