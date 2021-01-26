---
description: Vinhetas são imagens criadas com a Criação de imagens do Dynamic Media para uso com a Renderização de imagens.
solution: Experience Manager
title: Vinhetas
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---


# Vinhetas{#vignettes}

Vinhetas são imagens criadas com a Criação de imagens do Dynamic Media para uso com a Renderização de imagens.

O IR suporta dois tipos básicos de vinhetas, *2D* e *3D*. As cenas da sala normalmente são vinhetas 3D que podem renderizar reflexos, enquanto a maioria das outras cenas, como vestuário ou estofo, são normalmente vinhetas 2D que não têm capacidade de renderização de reflexo.

As vinhetas contêm uma *visualização* e uma hierarquia de *objetos*.

A visualização é o container da imagem principal, mapas de iluminação compartilhada, mapas de reflexão compartilhada e outros dados associados à imagem inteira.

A hierarquia de objetos consiste em *grupos de objetos*, *objetos padrão* e *objetos sobrepostos*.

Cada objeto padrão controla uma área da imagem de visualização, definida com uma *máscara* em escala cinza. As máscaras de objetos padrão nunca se sobrepõem. Objetos padrão não podem ser ocultos diretamente, mas podem ser cobertos parcial ou totalmente por objetos sobrepostos. A maioria ou todos os objetos em uma vinheta típica são objetos padrão.

Coloque objetos em camadas sobre a imagem da visualização e uns sobre os outros. A ordem de sobreposição é definida por um valor z atribuído ao objeto. Objetos sobrepostos são úteis quando partes de uma cena precisam ser mostradas ou ocultadas dinamicamente.

Vários tipos de objetos são suportados (padrão e sobrepostos), cada um com seu próprio propósito distinto:

* **Objetos**  planares (em vinhetas 3D) e objetos **** planos (em vinhetas 2D) aceitam materiais de textura repetíveis. Normalmente, são usados para pisos, contraptops e outras superfícies planas que exigem apenas o mapeamento de perspectiva.

* **O objeto de linha** flutuante tem superfícies curvas em forma suave, como estofamento, e são ocasionalmente usados para objetos de vestuário também. Eles podem ser usados em vinhetas 2D e 3D e, se forem totalmente criados, participarão da renderização do reflexo.
* **Objetos não texturizáveis só** permitem alterações de cores. Elas são permitidas em vinhetas 2D e 3D. Eles são inerentemente não texturizáveis ou podem ser um objeto plano ou flanfrado com um sinalizador especial &quot;Sem textura&quot; definido. Isso é útil em vinhetas 3D para permitir que os objetos participem da renderização de reflexão, mesmo que o objeto aceite somente materiais de cor sólida.
* **Os** objetos de rascunho são melhor usados para objetos de malha com dobras e rugas, como itens de vestuário. Como os objetos em linhas continuadas, eles podem ser usados em vinhetas 2D e 3D, embora o aplicativo em vinhetas 3D seja limitado.
* **Os** objetos de parede são semelhantes aos objetos planares e são suportados apenas em vinhetas 3D. Eles têm informações de layout especiais que permitem a aplicação de dois acabamentos de parede diferentes (superior e inferior) e até três materiais de borda de parede. Quando criados corretamente, os materiais aplicados às paredes fluirão de forma precisa e contínua entre as paredes adjacentes, para aplicativos realistas de borda de papel de parede/parede. Objetos de mural não suportam rotação de textura.
* **Os** objetos de gabinete são permitidos apenas em vinhetas 3D. Eles são usados para criar armários de cozinha e banho com requisitos complexos de layout. Objetos de gabinete aceitam texturas repetíveis, bem como arquivos *estilo gabinete* com imagens redimensionáveis no painel gabinete.

Além dos tipos básicos de objetos, dois tipos especiais de objetos sobrepostos são suportados:

* **Objetos de sobreposição estática** são objetos que não aceitam materiais. Elas são permitidas em vinhetas 2D e 3D. Eles são úteis para acessórios removíveis em uma cena de sala, para sombras projetadas atrás de objetos sobrepostos renderizáveis e aplicativos semelhantes.
* **A janela que cobre** objetos de quadro fornece informações de posicionamento para aplicar arquivos de estilo de revestimento de janela, que são criados independentemente da vinheta e podem ser compartilhados entre vinhetas.

Os objetos são coletados em *grupos de objetos*, semelhantes a um sistema de arquivos. O agrupamento normalmente se baseia na estrutura dos objetos físicos que eles representam (por exemplo, um grupo &#39;Todos os gabinetes&#39; pode conter &#39;Gabinetes de base&#39; e &#39;Gabinetes de mural&#39;). É permitido qualquer número de níveis de grupo. O agrupamento suporta a aplicação de materiais a vários objetos semelhantes.

* [Coordenadas de cena](c-ir-scene-coordinates.md)
* [Resolução de material](c-ir-material-resolution.md)
