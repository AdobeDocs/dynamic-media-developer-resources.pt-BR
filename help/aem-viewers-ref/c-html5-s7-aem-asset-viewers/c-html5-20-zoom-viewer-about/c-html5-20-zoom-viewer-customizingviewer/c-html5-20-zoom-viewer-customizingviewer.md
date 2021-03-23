---
description: Toda a personalização visual e a maioria dos comportamentos do Visualizador de Zoom é feita criando um CSS personalizado.
keywords: responsivo
seo-description: Toda a personalização visual e a maioria dos comportamentos do Visualizador de Zoom é feita criando um CSS personalizado.
seo-title: Personalização do Visualizador de Zoom
solution: Experience Manager
title: Personalização do Visualizador de Zoom
uuid: 7ecbc4cc-b5c0-4f4a-b747-03c484de6851
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '1354'
ht-degree: 0%

---


# Personalizar Visualizador de Zoom{#customizing-zoom-viewer}

Toda a personalização visual e a maioria dos comportamentos do Visualizador de Zoom é feita criando um CSS personalizado.

O fluxo de trabalho sugerido é pegar o arquivo CSS padrão do visualizador apropriado, copiá-lo para um local diferente, personalizá-lo e especificar o local do arquivo personalizado no comando `style=`.

Arquivos CSS padrão podem ser encontrados no seguinte local:

`<s7_viewers_root>/html5/ZoomViewer_light.css`

O visualizador é fornecido com dois arquivos CSS prontos para uso, para esquemas de cores &quot;claro&quot; e &quot;escuro&quot;. A versão &quot;claro&quot; é usada por padrão, mas você pode alternar para a versão &quot;escura&quot; usando o seguinte CSS padrão:

`<s7_viewers_root>/html5/ZoomViewer_dark.css`

O arquivo CSS personalizado deve conter as mesmas declarações de classe que a padrão. Se uma declaração de classe for omitida, o visualizador não funcionará corretamente porque não fornece estilos padrão incorporados para elementos da interface do usuário.

Outra maneira de fornecer regras de CSS personalizadas é usar estilos incorporados diretamente na página da Web ou em uma das regras de CSS externas vinculadas.

Ao criar CSS personalizado, lembre-se de que o visualizador atribui a classe `.s7zoomviewer` ao elemento DOM do contêiner. Se você estiver usando um arquivo CSS externo passado com o comando `style=`, use a classe `.s7zoomviewer` como classe pai no seletor descendente para suas regras CSS. Se você estiver fazendo estilos incorporados na página da Web, qualifique também esse seletor com uma ID do elemento DOM do contêiner da seguinte maneira:

`#<containerId>.s7zoomviewer`

## Criando CSS responsivo projetado {#section-0bb49aca42d242d9b01879d5ba59d33b}

É possível direcionar diferentes dispositivos e tamanhos de incorporação no CSS para fazer com que o conteúdo seja exibido de forma diferente, dependendo do dispositivo de um usuário ou de um layout de página da Web específico. Isso inclui, mas não está limitado a, diferentes layouts, tamanhos de elementos da interface do usuário e resolução do trabalho artístico.

O visualizador aceita dois mecanismos para criar CSS responsivo projetado: Marcadores CSS e consultas de mídia CSS padrão. Você pode usá-los independentemente ou juntos.

**Marcadores CSS**

Para auxiliar na criação de CSS responsivo projetado, o visualizador aceita marcadores CSS. São classes CSS especiais que são atribuídas dinamicamente ao elemento do contêiner do visualizador de nível superior com base no tamanho do visualizador de tempo de execução e no tipo de entrada usado no dispositivo atual.

O primeiro grupo de marcadores CSS inclui `.s7size_large`, `.s7size_medium` e `.s7size_small` classes. Eles são aplicados com base na área de tempo de execução do contêiner do visualizador. Se a área do visualizador for igual ou maior que o tamanho de um monitor de desktop comum, `.s7size_large` será usado; se a área estiver próxima de um tablet comum, `.s7size_medium` será atribuído. Para áreas semelhantes a telas de celular, `.s7size_small` é definido. O objetivo principal desses marcadores CSS é criar diferentes layouts de interface do usuário para diferentes telas e tamanhos de visualizador.

O segundo grupo de marcadores CSS contém `.s7mouseinput` e `.s7touchinput`. `.s7touchinput` é definido se o dispositivo atual tiver recursos de entrada por toque; caso contrário,  `.s7mouseinput` será usado. Esses marcadores são destinados principalmente a criar elementos de entrada da interface do usuário com tamanhos de tela diferentes para tipos de entrada diferentes, pois normalmente a entrada por toque requer elementos maiores. Caso o dispositivo tenha recursos de entrada e toque do mouse, `.s7touchinput` é definido e o visualizador renderiza uma interface de usuário fácil de tocar.

A amostra de CSS a seguir define o tamanho do botão de zoom em 28 x 28 pixels em sistemas com entrada de mouse e em 56 x 56 pixels em dispositivos de toque. Além disso, ele oculta completamente o botão se o tamanho do visualizador for muito pequeno:

```
.s7zoomviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7zoomviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7zoomviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

Para direcionar dispositivos com densidade de pixels diferente, você precisa usar consultas de mídia CSS. O seguinte bloco de consulta de mídia contém CSS específico para telas de alta densidade:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

Usar marcadores CSS é a maneira mais flexível de criar CSS projetado responsivo, pois permite direcionar não apenas o tamanho da tela do dispositivo, mas o tamanho real do visualizador, o que é útil para layouts de design responsivos.

Você pode usar o arquivo CSS do visualizador padrão como exemplo de uma abordagem de Marcadores CSS.

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

## Sprites CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

Muitos elementos da interface do usuário do visualizador são estilizados usando a arte-final de bitmap e têm mais de um estado visual distinto. Um bom exemplo é um botão que normalmente tem pelo menos 3 estados diferentes: &quot;para cima&quot;, &quot;para cima&quot; e &quot;para baixo&quot;. Cada estado requer sua própria arte bitmap atribuída.

Com uma abordagem clássica ao estilo, o CSS teria uma referência separada para o arquivo de imagem individual no servidor para cada estado do elemento da interface do usuário. Esta é uma amostra de CSS para o botão de zoom de estilo:

```
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

A desvantagem dessa abordagem é que o usuário final apresenta cintilação ou resposta retardada da interface do usuário quando o elemento interagiu pela primeira vez. Essa ação ocorre porque a arte-final da imagem do novo estado do elemento ainda não foi baixada. Além disso, essa abordagem pode ter um impacto negativo no desempenho devido ao aumento do número de chamadas HTTP para o servidor.

Os sprites CSS são uma abordagem diferente, na qual a arte-final de imagem de todos os estados do elemento é combinada em um único arquivo PNG chamado de &quot;sprite&quot;. Esse &quot;sprite&quot; tem todos os estados visuais para o determinado elemento posicionado um após o outro. Ao estilizar um elemento da interface do usuário com sprites, a mesma imagem de sprite é referenciada para todos os estados diferentes no CSS. Além disso, a propriedade `background-position` é usada para cada estado para especificar qual parte da imagem &quot;sprite&quot; é usada. Você pode estruturar uma imagem &quot;sprite&quot; de qualquer maneira adequada. Os visualizadores normalmente o têm empilhado verticalmente. Abaixo está um exemplo baseado em &quot;sprite&quot; de como colocar o mesmo botão de zoom acima:

```
.s7zoomviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
}
```

## Notas e conselhos gerais sobre estilo {#section-95855dccbbc444e79970f1aaa3260b7b}

* Ao personalizar a interface do usuário do visualizador com CSS, o uso da regra `!IMPORTANT` não é compatível com os elementos do visualizador de estilo. Especificamente, a regra `!IMPORTANT` não deve ser usada para substituir qualquer estilo padrão ou de tempo de execução fornecido pelo visualizador ou pelo SDK do visualizador. Isso pode afetar o comportamento de componentes adequados. Em vez disso, você deve usar seletores de CSS com a especificidade adequada para definir propriedades de CSS documentadas neste guia de referência.
* Todos os caminhos para ativos externos dentro do CSS são resolvidos em relação ao local do CSS, não no local da página HTML do visualizador. Esteja ciente dessa regra ao copiar o CSS padrão para um local diferente. Copie também os ativos padrão ou atualize caminhos no CSS personalizado.
* O formato preferido para a arte-final de bitmap é PNG.
* A arte-final do bitmap é atribuída aos elementos da interface do usuário usando a propriedade `background-image` .
* As propriedades `width` e `height` de um elemento da interface do usuário definem o tamanho lógico. O tamanho do bitmap passado para `background-image` não afeta o tamanho lógico.
* Para usar a alta densidade de pixels de telas de alta resolução como Retina, especifique a arte-final de bitmap duas vezes maior que o tamanho do elemento da interface de usuário lógica. Em seguida, aplique a propriedade `-webkit-background-size:contain` para dimensionar o plano de fundo para baixo no tamanho do elemento da interface do usuário lógica.
* Para remover um botão da interface do usuário, adicione `display:none` a sua classe CSS.
* Você pode usar vários formatos para o valor de cor que o CSS suporta. Se precisar de transparência, use o formato `rgba(R,G,B,A)`. Caso contrário, você poderá usar o formato `#RRGGBB`.

## Elementos Comuns Da Interface Do Usuário {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Veja a seguir a documentação de referência dos elementos da interface do usuário que se aplica ao Visualizador de vídeo:
