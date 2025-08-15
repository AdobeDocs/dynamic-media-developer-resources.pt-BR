---
title: Vinhetas
description: As vinhetas são imagens criadas com a criação de imagem do Dynamic Media para uso com renderização de imagem.
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

As vinhetas são imagens criadas com a criação de imagem do Dynamic Media para uso com renderização de imagem.

O IR suporta dois tipos básicos de vinhetas: *2D* e *3D*. Cenas de quartos normalmente são vinhetas 3D que podem renderizar reflexos, enquanto a maioria das outras cenas, como vestuário ou estofamento, são normalmente vinhetas 2D que não têm capacidade de renderização de reflexão.

As vinhetas contêm uma *exibição* e uma hierarquia de *objetos*.

A exibição é o contêiner da imagem principal, mapas de iluminação compartilhados, mapas de reflexão compartilhados e outros dados associados à imagem inteira.

A hierarquia de objetos consiste em *grupos de objetos*, *objetos padrão* e *objetos de sobreposição*.

Cada objeto padrão controla uma área da imagem de exibição, definida com uma *máscara* de escala de cinza. As máscaras de objetos padrão nunca se sobrepõem. Objetos padrão não podem ser ocultos diretamente, mas podem ser parcial ou totalmente cobertos por objetos sobrepostos. A maioria ou todos os objetos em uma vinheta típica são objetos padrão.

Sobrepor a camada de objetos na parte superior da imagem da exibição e entre si. A ordem de sobreposição é definida por um valor z atribuído ao objeto. Objetos sobrepostos são úteis quando partes de uma cena devem ser exibidas ou ocultadas dinamicamente.

Vários tipos de objetos são suportados (padrão e sobreposição), com cada um tendo sua própria finalidade distinta:

* **Objetos planos** (em vinhetas 3D) e **objetos planos** (em vinhetas 2D) aceitam materiais de textura repetíveis. Normalmente, são usados para pisos, bancadas e outras superfícies planas que exigem apenas mapeamento de perspectiva.
* **Objetos de linha de fluxo** mapeiam superfícies curvas em forma suave, como estofos, e também são usados ocasionalmente para objetos de vestuário. Eles podem ser usados em vinhetas 2D e 3D e, se forem totalmente criados, participam da renderização de reflexão.
* **Objetos não texturáveis** permitem somente alterações de cores. Eles são permitidos em vinhetas 2D e 3D. Eles são inerentemente não texturáveis ou podem ser um objeto planar ou fluxograma com um sinalizador especial &quot;Sem Textura&quot; definido. Esse método é útil em vinhetas 3D para permitir que os objetos participem da renderização de reflexão, mesmo que o objeto aceite apenas materiais de cores sólidas.
* **Objetos de esboço** são mais adequados para objetos de malha com dobras e rugas, como itens de vestuário. Como objetos de linha de fluxo, eles podem ser usados em vinhetas 2D e 3D, embora a aplicação em vinhetas 3D seja limitada.
* **Objetos de parede** são semelhantes a objetos planos e só têm suporte em vinhetas 3D. Eles têm informações de layout especiais que permitem a aplicação de dois acabamentos de parede diferentes (superior e inferior) e até três materiais de borda de parede. Quando adequadamente criados, os materiais aplicados às paredes fluem com precisão e perfeição entre as paredes adjacentes, para aplicações realistas de borda de papel de parede/papel de parede. Os objetos de parede não oferecem suporte à rotação de textura.
* **Objetos de gabinete** são permitidos somente em vinhetas 3D. Eles são usados para criar armários de cozinha e banheiro com requisitos complexos de layout. Os objetos de gabinete aceitam texturas repetíveis e *arquivos de estilo de gabinete* especialmente criados contendo imagens redimensionáveis do painel de gabinete.

Além dos tipos de objetos básicos, há suporte para dois tipos especiais de objetos sobrepostos:

* **Objetos de sobreposição estática** são objetos que não aceitam materiais. Eles são permitidos em vinhetas 2D e 3D. Eles são úteis para acessórios removíveis na cena de uma sala, para sombras projetadas atrás de objetos de sobreposição renderizáveis e aplicativos semelhantes.
* **Os objetos de quadro de cobertura de janela** fornecem informações de posicionamento para aplicar arquivos de estilo de coberturas de janela, que são criados independentemente da vinheta e podem ser compartilhados entre vinhetas.

Os objetos são coletados em *grupos de objetos*, semelhante a um sistema de arquivos. O agrupamento normalmente se baseia na estrutura dos objetos físicos que eles representam (por exemplo, um grupo &quot;Todos os gabinetes&quot; pode conter &quot;Gabinetes de base&quot; e &quot;Gabinetes de parede&quot;). Qualquer número de níveis de grupo é permitido. O agrupamento suporta a aplicação de materiais a múltiplos objetos semelhantes.

* [Coordenadas da cena](c-ir-scene-coordinates.md)
* [Resolução de material](c-ir-material-resolution.md)
