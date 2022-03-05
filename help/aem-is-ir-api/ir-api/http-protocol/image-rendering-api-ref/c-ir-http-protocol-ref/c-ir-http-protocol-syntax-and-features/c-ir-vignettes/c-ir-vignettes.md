---
title: Vinhetas
description: Vinhetas são imagens criadas com o Dynamic Media Image Authoring para uso com o Image Rendering.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5e1be99c-58c0-4e3c-bc57-7be5fa25ccef
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# Vinhetas{#vignettes}

Vinhetas são imagens criadas com o Dynamic Media Image Authoring para uso com o Image Rendering.

A IR suporta dois tipos básicos de vinhetas: *2D* e *3D*. As cenas da sala normalmente são vinhetas 3D que podem renderizar reflexos, enquanto a maioria das outras cenas, como vestuário ou estofo, normalmente são vinhetas 2D que não têm capacidade de renderização de reflexo.

As vinhetas contêm uma *exibir* e uma hierarquia de *objetos*.

A exibição é o contêiner da imagem principal, mapas de iluminação compartilhada, mapas de reflexão compartilhados e outros dados associados à imagem inteira.

A hierarquia de objetos consiste em *grupos de objetos*, *objetos padrão* e *objetos de sobreposição*.

Cada objeto padrão controla uma área da imagem de exibição, definida com uma escala de cinza *máscara*. As máscaras de objetos padrão nunca se sobrepõem. Os objetos padrão não podem ser ocultos diretamente, mas podem ser cobertos parcial ou totalmente por objetos sobrepostos. A maioria ou todos os objetos em uma vinheta típica são objetos padrão.

Sobrepor objetos em camadas na parte superior da imagem de exibição e entre si. A ordem de sobreposição é definida por um valor z atribuído ao objeto. Objetos de sobreposição são úteis quando partes de uma cena devem ser mostradas ou ocultas dinamicamente.

Vários tipos de objetos são suportados (padrão e sobreposição), cada um com seu próprio propósito distinto:

* **Objetos planos** (em vinhetas 3D) e **objetos planos** (em vinhetas 2D) aceitar materiais de textura repetíveis. Normalmente, são usadas para pisos, contratops e outras superfícies planas que exigem apenas o mapeamento de perspectiva.
* **Objetos Flowline** mapeie superfícies curvas em forma suave, como estofo, e são ocasionalmente usadas para objetos de vestuário também. Elas podem ser usadas em vinhetas 2D e 3D e, se criadas totalmente, participam da renderização de reflexão.
* **Objetos não texturizáveis** permitir apenas alterações de cor. Elas são permitidas em vinhetas 2D e 3D. Eles são inerentemente não texturizáveis ou podem ser um objeto plano ou flowline com um sinalizador especial &quot;Sem textura&quot; definido. Esse método é útil em vinhetas 3D para permitir que objetos participem da renderização de reflexão, mesmo que o objeto aceite apenas materiais de cor sólida.
* **Objetos de rascunho** são mais usados para objetos de malha com dobras e rugas, como itens de vestuário. Como objetos flowline, eles podem ser usados em vinhetas 2D e 3D, embora o aplicativo em vinhetas 3D seja limitado.
* **Objetos de parede** são semelhantes a objetos planares e são compatíveis apenas com vinhetas 3D. Eles têm informações especiais de layout que permitem a aplicação de dois acabamentos de parede diferentes (superior e inferior) e até três materiais de borda de parede. Quando criados corretamente, os materiais aplicados nas paredes fluem com precisão e facilidade entre paredes adjacentes, para aplicações realistas de borda de papel de parede/parede. Objetos de mural não suportam rotação de textura.
* **Objetos de gabinete** são permitidas somente em vinhetas 3D. Eles são usados para criar armários de cozinha e banho com requisitos complexos de layout. Objetos de gabinete aceitam texturas repetíveis e especialmente criadas *arquivos de estilo do gabinete* contendo imagens redimensionáveis do painel do gabinete.

Além dos tipos básicos de objetos, dois tipos especiais de objetos de sobreposição são suportados:

* **Objetos de sobreposição estática** são objetos que não aceitam materiais. Elas são permitidas em vinhetas 2D e 3D. Eles são úteis para acessórios removíveis em uma cena de sala, para sombras traseiras de objetos de sobreposição renderizáveis e aplicativos semelhantes.
* **Objetos de estrutura de revestimento de janelas** forneça informações de posicionamento para aplicar arquivos de estilo de cobertura de janela, que são criados independentemente da vinheta e podem ser compartilhados entre vinhetas.

Os objetos são coletados em *grupos de objetos*, semelhante a um sistema de arquivos. O agrupamento é normalmente baseado na estrutura dos objetos físicos que eles representam (por exemplo, um grupo &#39;Todos os gabinetes&#39; pode conter &#39;Gabinetes base&#39; e &#39;Gabinetes de mural&#39;). É permitido qualquer número de níveis de grupo. O agrupamento suporta a aplicação de materiais em vários objetos semelhantes.

* [Coordenadas da cena](c-ir-scene-coordinates.md)
* [Resolução de material](c-ir-material-resolution.md)
