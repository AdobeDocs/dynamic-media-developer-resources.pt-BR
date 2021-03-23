---
description: Toda personalização visual e a maioria dos comportamentos do Visualizador de carrossel são feitos com a criação de um CSS personalizado.
keywords: responsivo
seo-description: Toda personalização visual e a maioria dos comportamentos do Visualizador de carrossel são feitos com a criação de um CSS personalizado.
seo-title: Personalizar o Visualizador de carrossel
solution: Experience Manager
title: Personalizar o Visualizador de carrossel
uuid: a35dac3c-8785-42bf-8284-e400128f213c
feature: Dynamic Media Classic,Visualizadores,SDK/API,Banners em carrossel
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '1368'
ht-degree: 0%

---


# Personalizar o Visualizador de carrossel{#customizing-carousel-viewer}

Toda personalização visual e a maioria dos comportamentos do Visualizador de carrossel são feitos com a criação de um CSS personalizado.

O fluxo de trabalho sugerido é pegar o arquivo CSS padrão do visualizador apropriado, copiá-lo para um local diferente, personalizá-lo e especificar o local do arquivo personalizado no comando `style=`.

Arquivos CSS padrão podem ser encontrados no seguinte local:

`<s7viewers_root>/etc/dam/viewers/s7viewers/html5/CarouselViewer_dotted_light.css`

O visualizador é fornecido com quatro arquivos CSS prontos para uso, para indicadores numéricos e de conjunto pontilhado, cada um em um esquema de cores &quot;claro&quot; e &quot;escuro&quot;. A versão &quot;Luz pontilhada&quot; é usada por padrão, mas é fácil alternar para uma versão diferente usando CSS padrão diferente e definindo o parâmetro `SetIndicator.mode`. Outros CSS padrão podem ser encontrados no seguinte local:

`<s7_viewers_root>/html5/CarouselViewer_dotted_dark.css`

`<s7_viewers_root>/html5/CarouselViewer_numeric_dark.css`

`<s7_viewers_root>/html5/CarouselViewer_numeric_light.css`

O arquivo CSS personalizado deve conter as mesmas declarações de classe que a padrão. Se uma declaração de classe for omitida, o visualizador não funcionará corretamente porque não fornece estilos padrão incorporados para elementos da interface do usuário.

Uma maneira alternativa de fornecer regras de CSS personalizadas é usar estilos incorporados diretamente na página da Web ou em uma das regras de CSS externas vinculadas.

Ao criar CSS personalizado, lembre-se de que o visualizador atribui a classe `.s7carouselviewer` ao elemento DOM do contêiner. Se estiver usando um arquivo CSS externo passado com o comando `style=`, use a classe `.s7carouselviewer` como classe pai no seletor descendente para suas regras CSS. Se você estiver adicionando estilos incorporados na página da Web, qualifique também esse seletor com uma ID do elemento DOM do contêiner da seguinte maneira:

`#<containerId>.s7carouselviewer`

## Criando CSS responsivo projetado {#section-0bb49aca42d242d9b01879d5ba59d33b}

É possível direcionar diferentes dispositivos e tamanhos de incorporação no CSS para fazer com que o conteúdo seja exibido de forma diferente, dependendo do dispositivo de um usuário ou de um layout de página da Web específico. Isso inclui, mas não está limitado a, diferentes layouts, tamanhos de elementos da interface do usuário e resolução do trabalho artístico.

O visualizador aceita dois mecanismos para criar CSS responsivo projetado: Marcadores CSS e consultas de mídia CSS padrão. Você pode usá-los independentemente ou juntos.

**Marcadores CSS**

Para auxiliar na criação de CSS responsivo projetado, o visualizador aceita marcadores CSS. Essas são classes CSS especiais atribuídas dinamicamente ao elemento do contêiner do visualizador de nível superior. Elas se baseiam no tamanho do visualizador de tempo de execução e no tipo de entrada usado no dispositivo atual.

O primeiro grupo de marcadores CSS contém `.s7size_large`, `.s7size_medium` e `.s7size_small` classes. Eles são aplicados com base na área de tempo de execução do contêiner do visualizador. Por exemplo, se a área do visualizador for igual ou maior que o tamanho de um monitor de desktop comum, use `.s7size_large`. Se a área estiver próxima de um tablet comum, atribua `.s7size_medium`. Para áreas semelhantes a telas de telefones celulares, use `.s7size_small`. O objetivo principal desses marcadores CSS é criar diferentes layouts de interface do usuário para diferentes telas e tamanhos de visualizador.

O segundo grupo de marcadores CSS contém `.s7mouseinput` e `.s7touchinput`. O marcador de CSS `.s7touchinput` é definido se o dispositivo atual for capaz de entrar por toque. Caso contrário, `.s7mouseinput` será usado. Esses marcadores são destinados principalmente a criar elementos de entrada da interface do usuário com tamanhos de tela diferentes para tipos de entrada diferentes, pois normalmente a entrada por toque requer elementos maiores.

A amostra de CSS a seguir define o tamanho do botão de zoom em 28 x 28 pixels em sistemas com entrada de mouse e em 56 x 56 pixels em dispositivos de entrada de toque. Se o visualizador for dimensionado ainda menor, ele será definido como 20 x 20 pixels.

```
.s7carouselviewer.s7mouseinput .s7imagemapeffect .s7icon { 
    width:28px; 
    height:28px; 
} 
.s7carouselviewer.s7touchinput .s7imagemapeffect .s7icon { 
    width:56px; 
    height:56px; 
} 
.s7carouselviewer.s7size_small .s7imagemapeffect .s7icon { 
    width:20px; 
    height:20px; 
}
```

Para direcionar dispositivos com densidade de pixels diferente, você precisa usar consultas de mídia CSS. O seguinte bloco de consulta de mídia contém CSS específico para telas de alta densidade:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

Usar marcadores CSS é a maneira mais flexível de criar CSS projetado responsivo, pois permite direcionar não apenas o tamanho da tela do dispositivo, mas o tamanho real do visualizador, o que é útil para layouts de design responsivos.

Você pode usar o arquivo CSS do visualizador padrão como exemplo de uma abordagem de marcadores CSS.

**Consultas de mídia CSS**

Você também pode realizar a detecção de dispositivos usando consultas de mídia CSS puras. Tudo que é delimitado em um determinado bloco de consulta de mídia é aplicado somente quando é executado em um dispositivo correspondente.

Quando aplicado a visualizadores móveis, você usa quatro consultas de mídia CSS, definidas em seu CSS, na ordem listada abaixo:

1. Contém apenas regras específicas para todos os dispositivos de toque.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
   { 
   }
   ```

1. Contém apenas regras específicas para tablets com telas de alta resolução.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. Contém apenas regras específicas para todos os telefones celulares.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. Contém apenas regras específicas para telefones celulares com telas de alta resolução.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

Usando uma abordagem de consultas de mídia, você deve organizar o CSS com detecção de dispositivo da seguinte maneira:

* Primeiro, a seção específica do desktop define todas as propriedades que são específicas do desktop ou comuns a todas as telas.
* E segundo, as quatro consultas de mídia seguem a ordem definida acima e fornecem regras de CSS específicas para o tipo de dispositivo correspondente.

Não há necessidade de duplicar todo o CSS do visualizador em cada consulta de mídia. Somente as propriedades específicas de determinados dispositivos são redefinidas em uma consulta de mídia.

## Primatas CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

Muitos elementos da interface do usuário do visualizador são estilizados usando a arte-final de bitmap e têm mais de um estado visual distinto. Um bom exemplo é um botão que normalmente tem pelo menos três estados diferentes: `up`, `over` e `down`. Cada estado requer sua própria arte bitmap atribuída.

Com uma abordagem clássica ao estilo, o CSS teria uma referência separada ao arquivo de imagem individual no servidor para cada estado do elemento da interface do usuário. Veja a seguir uma amostra de CSS para estilizar um botão de zoom:

```
.s7carouselviewer .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
} 
.s7carouselviewer .s7imagemapeffect .s7icon:hover { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

A desvantagem dessa abordagem é que o usuário final apresenta cintilação ou resposta retardada da interface do usuário quando o elemento interagiu pela primeira vez. Essa ação ocorre porque a arte-final da imagem do novo estado do elemento ainda não foi baixada. Além disso, essa abordagem pode ter um impacto negativo no desempenho devido ao aumento do número de chamadas HTTP para o servidor.

Os sprites CSS são uma abordagem diferente, na qual a arte-final de imagem de todos os estados do elemento é combinada em um único arquivo PNG chamado de &quot;sprite&quot;. Esse &quot;sprite&quot; tem todos os estados visuais para o determinado elemento posicionado um após o outro. Ao estilizar um elemento da interface do usuário com sprites, a mesma imagem de sprite é referenciada para todos os estados diferentes no CSS. Além disso, a propriedade `background-position` é usada para cada estado para especificar qual parte da imagem &quot;sprite&quot; é usada. Você pode estruturar uma imagem &quot;sprite&quot; de qualquer maneira adequada. Os visualizadores normalmente o têm empilhado verticalmente.

Veja a seguir um exemplo baseado em &quot;sprite&quot; de como colocar o mesmo ícone de ponto de acesso:

```
.s7carouselviewer .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
background-position: -0px -56px; width: 56px; height: 56px; 
} 
.s7carouselviewer .s7imagemapeffect .s7icon:hover { 
background-position: -0px -0px; width: 56px; height: 56px; 
}
```

## Notas e conselhos gerais sobre estilo {#section-95855dccbbc444e79970f1aaa3260b7b}

* Ao personalizar a interface do usuário do visualizador com CSS, o uso da regra `!IMPORTANT` não é compatível com os elementos do visualizador de estilo. Especificamente, a regra `!IMPORTANT` não deve ser usada para substituir qualquer estilo padrão ou de tempo de execução fornecido pelo visualizador ou pelo SDK do visualizador. O motivo para isso é que pode afetar o comportamento de componentes adequados. Em vez disso, você deve usar seletores de CSS com a especificidade adequada para definir propriedades de CSS documentadas neste guia Referência de visualizadores .
* Todos os caminhos para ativos externos dentro do CSS são resolvidos em relação ao local do CSS, não no local da página HTML do visualizador. Esteja ciente dessa regra ao copiar o CSS padrão para um local diferente. Copie também os ativos padrão ou atualize todos os caminhos no CSS personalizado.
* O formato preferido para a arte-final de bitmap é PNG.
* A arte-final do bitmap é atribuída aos elementos da interface do usuário usando a propriedade `background-image` .
* As propriedades `width` e `height` de um elemento da interface do usuário definem o tamanho lógico. O tamanho do bitmap passado para `background-image` não afeta seu tamanho lógico.
* Para usar a alta densidade de pixels de telas de alta resolução como Retina, especifique a arte-final de bitmap duas vezes maior que o tamanho do elemento da interface de usuário lógica. Em seguida, aplique a propriedade `-webkit-background-size:contain` para dimensionar o plano de fundo para baixo no tamanho do elemento da interface do usuário lógica.
* Para remover um botão da interface do usuário, adicione `display:none` a sua classe CSS.
* Você pode usar vários formatos para o valor de cor que o CSS suporta. Se precisar de transparência, use o formato `rgba(R,G,B,A)`. Caso contrário, você poderá usar o formato `#RRGGBB`.

## Elementos comuns da interface do usuário {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Veja a seguir a documentação de referência dos elementos da interface do usuário que se aplica ao Visualizador de imagem de vídeo:
