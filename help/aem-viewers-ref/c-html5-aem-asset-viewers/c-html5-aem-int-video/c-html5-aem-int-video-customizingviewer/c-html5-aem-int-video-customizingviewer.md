---
description: Toda personalização visual e a maioria dos comportamentos do Visualizador de vídeo interativo são feitos com a criação de um CSS personalizado.
keywords: responsive
seo-description: Toda personalização visual e a maioria dos comportamentos do Visualizador de vídeo interativo são feitos com a criação de um CSS personalizado.
seo-title: Personalização do Visualizador de vídeo interativo
solution: Experience Manager
title: Personalização do Visualizador de vídeo interativo
topic: Dynamic Media
uuid: a24e7ada-c874-468b-ac44-a51d581d4479
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '1410'
ht-degree: 0%

---


# Personalização do Visualizador de vídeo interativo{#customizing-interactive-video-viewer}

Toda personalização visual e a maioria dos comportamentos do Visualizador de vídeo interativo são feitos com a criação de um CSS personalizado.

O fluxo de trabalho sugerido é pegar o arquivo CSS padrão para o visualizador apropriado, copiá-lo para um local diferente, personalizá-lo e especificar o local do arquivo personalizado no comando `style=`.

Os arquivos CSS padrão podem ser encontrados no seguinte local:

`<s7_viewers_root>/html5/InteractiveVideoViewer_dark.css`

O visualizador é fornecido com dois arquivos CSS prontos para uso, para esquemas de cores &quot;claro&quot; e &quot;escuro&quot;. A versão &quot;escura&quot; é usada por padrão, mas é fácil alternar para a versão &quot;clara&quot; usando o seguinte CSS padrão:

`<s7_viewers_root>/html5/InteractiveVideoViewer_light.css`

O arquivo CSS personalizado deve conter as mesmas declarações de classe que a padrão. Se uma declaração de classe for omitida, o visualizador não funcionará corretamente porque não fornece estilos padrão incorporados para elementos da interface do usuário.

Uma maneira alternativa de fornecer regras CSS personalizadas é usar estilos incorporados diretamente na página da Web ou em uma das regras CSS externas vinculadas.

Ao criar CSS personalizado, lembre-se de que o visualizador atribui a classe `.s7interactivevideoviewer` ao elemento DOM do container. Se você estiver usando um arquivo CSS externo transmitido com o comando `style=`, use a classe `.s7interactivevideoviewer` como classe pai no seletor descendente para suas regras CSS. Se você estiver fazendo estilos incorporados na página da Web, qualifice adicionalmente este seletor com uma ID do elemento DOM do container da seguinte maneira:

`#<containerId>.s7interactivevideoviewer`

## Criação de CSS {#section-0bb49aca42d242d9b01879d5ba59d33b} projetado responsivo

É possível público alvo de diferentes dispositivos e tamanhos de incorporação no CSS para fazer com que seu conteúdo seja exibido de forma diferente dependendo do dispositivo do usuário ou de um layout de página da Web específico. Isso inclui, entre outros, diferentes layouts, tamanhos de elementos da interface do usuário e resolução da arte-final.

O visualizador suporta dois mecanismos de criação de CSS responsivo projetado: Marcadores CSS e query de mídia CSS padrão. Você pode usá-los independentemente ou juntos.

**Marcadores CSS**

Para auxiliar na criação de CSS responsivo projetado, o visualizador oferece suporte a marcadores CSS. São classes CSS especiais que são atribuídas dinamicamente ao elemento de container do visualizador de nível superior com base no tamanho do visualizador de tempo de execução e no tipo de entrada usado no dispositivo atual.

O primeiro grupo de marcadores CSS inclui `.s7size_large`, `.s7size_medium` e `.s7size_small` classes. Elas são aplicadas com base na área de tempo de execução do container do visualizador. Se a área do visualizador for igual ou maior que o tamanho de um monitor de área de trabalho comum, `.s7size_large` será usado; se a área estiver próxima a um tablet comum, `.s7size_medium` será atribuído. Para áreas semelhantes a telas de telefones celulares, `.s7size_small` é definido. O objetivo principal desses marcadores CSS é criar diferentes layouts de interface do usuário para telas e tamanhos de visualizador diferentes.

O segundo grupo de marcadores CSS contém `.s7mouseinput` e `.s7touchinput`. `.s7touchinput` é definido se o dispositivo atual tiver capacidades de entrada de toque; caso contrário,  `.s7mouseinput` será usado. Esses marcadores são destinados principalmente a criar elementos de entrada da interface do usuário com tamanhos de tela diferentes para tipos de entrada diferentes, pois normalmente a entrada de toque requer elementos maiores.

O terceiro grupo de marcadores CSS contém `.s7device_landscape` e `.s7device_portrait`. `.s7device_landscape` é definido se o dispositivo de toque estiver na orientação paisagem;  `.s7device_portrait` é usado quando o dispositivo de toque é girado para a orientação retrato. Esses marcadores CSS são destinados ao uso apenas em sistemas de desktop.

A amostra de CSS a seguir define o tamanho do botão play/pause como 28x28 pixels em sistemas com entrada do mouse e 56x56 pixels em dispositivos de toque. Além disso, oculta completamente o botão se o tamanho do visualizador for reduzido significativamente:

```
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7interactivevideoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7interactivevideoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

Neste próximo exemplo, a barra de controle de vídeo posicionará 138 pixels acima da parte inferior do visualizador se o dispositivo de toque estiver na orientação retrato e movê-lo para a parte inferior do visualizador em todos os outros casos:

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7controlbar, 
.s7interactivevideoviewer.s7mouseinput .s7controlbar { 
 bottom:0px; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7controlbar { 
 bottom:136px; 
}
```

Para público alvo de dispositivos com densidade de pixel diferente, é necessário usar query de mídia CSS. O seguinte bloco de query de mídia contém CSS específico para telas de alta densidade:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

O uso de marcadores CSS é a maneira mais flexível de criar um CSS responsivo projetado, pois permite público alvo não apenas do tamanho da tela do dispositivo, mas do tamanho real do visualizador, que é útil para layouts de design responsivos.

Você pode usar o arquivo CSS do visualizador padrão como exemplo de uma abordagem de marcadores CSS.

**Query de mídia CSS**

Você também pode realizar a detecção de dispositivos usando query de mídia CSS puros. Tudo o que está incluído em um determinado bloco de query de mídia é aplicado somente quando é executado em um dispositivo correspondente.

Quando aplicado aos Visualizadores móveis, use quatro query de mídia CSS, definidos em seu CSS, na ordem listada abaixo:

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

Usando uma abordagem de query de mídia, você deve organizar o CSS com detecção de dispositivos da seguinte maneira:

* Primeiro, a seção específica da área de trabalho define todas as propriedades que são específicas da área de trabalho ou comuns a todas as telas.
* Em segundo lugar, os quatro query de mídia seguem a ordem definida acima e fornecem regras de CSS específicas para o tipo de dispositivo correspondente.

Não há necessidade de duplicado do CSS do visualizador inteiro em cada query de mídia. Somente as propriedades específicas a determinados dispositivos são redefinidas em um query de mídia.

## Sprites CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

Muitos elementos da interface do usuário do visualizador têm estilo usando arte-final bitmap e mais de um estado visual distinto. Um bom exemplo é um botão que normalmente tem pelo menos 3 estados diferentes: &quot;para cima&quot;, &quot;para cima&quot; e &quot;para baixo&quot;. Cada estado requer sua própria arte-final de bitmap atribuída.

Com uma abordagem clássica ao estilo, o CSS teria uma referência separada ao arquivo de imagem individual no servidor para cada estado do elemento da interface do usuário. A seguir está um exemplo de CSS para estilizar um botão de tela cheia:

```
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

A desvantagem dessa abordagem é que o usuário final sofre oscilações ou retardamento da resposta da interface do usuário quando o elemento é interagido pela primeira vez. Essa ação ocorre porque a arte-final da imagem para o novo estado do elemento ainda não foi baixada. Além disso, essa abordagem pode ter um impacto negativo no desempenho devido ao aumento no número de chamadas HTTP para o servidor.

Os sprites CSS são uma abordagem diferente na qual a arte-final de imagem para todos os estados do elemento é combinada em um único arquivo PNG chamado de &quot;sprite&quot;. Tal &quot;sprite&quot; tem todos os estados visuais para um determinado elemento posicionado um após o outro. Ao estilizar um elemento da interface do usuário com sprites, a mesma imagem de sprite é referenciada para todos os estados diferentes no CSS. Além disso, a propriedade `background-position` é usada para cada estado para especificar qual parte da imagem &quot;sprite&quot; é usada. Você pode estruturar uma imagem &quot;sprite&quot; de qualquer maneira adequada. Os visualizadores normalmente o têm empilhado verticalmente. Abaixo está um exemplo baseado em &quot;sprite&quot; de como estilizar o mesmo botão de tela cheia anteriormente:

```
.s7interactivevideoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## Notas e conselhos gerais sobre estilo {#section-95855dccbbc444e79970f1aaa3260b7b}

* Ao personalizar a interface do usuário do visualizador com CSS, o uso da regra `!IMPORTANT` não é compatível com elementos do visualizador de estilo. Especificamente, a regra `!IMPORTANT` não deve ser usada para substituir qualquer estilo padrão ou de tempo de execução fornecido pelo visualizador ou pelo SDK do visualizador. Isso pode afetar o comportamento dos componentes apropriados. Em vez disso, você deve usar seletores de CSS com a especificidade adequada para definir as propriedades de CSS documentadas neste guia de referência.

* Todos os caminhos para ativos externos dentro do CSS são resolvidos em relação ao local do CSS, não ao local da página HTML do visualizador. Esteja ciente dessa regra ao copiar o CSS padrão para um local diferente. Copie também os ativos padrão ou atualize os caminhos no CSS personalizado.
* O formato preferido para a arte-final bitmap é PNG.
* A arte-final bitmap é atribuída aos elementos da interface do usuário usando a propriedade `background-image`.
* As propriedades `width` e `height` de um elemento da interface do usuário definem seu tamanho lógico. O tamanho do bitmap passado para `background-image` não afeta o tamanho lógico.

* Para usar a alta densidade de pixels de telas de alta resolução, como Retina, especifique a arte-final bitmap duas vezes maior que o tamanho do elemento lógico da interface do usuário. Em seguida, aplique a propriedade `-webkit-background-size:contain` para dimensionar o plano de fundo para baixo no tamanho do elemento da interface do usuário lógica.
* Para remover um botão da interface do usuário, adicione `display:none` à sua classe CSS.
* Você pode usar vários formatos para valores de cor compatíveis com CSS. Se precisar de transparência, use o formato `rgba(R,G,B,A)`. Caso contrário, você pode usar o formato `#RRGGBB`.

## Elementos Comuns da Interface do Usuário {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

A seguir estão os elementos da interface do usuário que fazem referência à documentação que se aplica ao Visualizador de vídeo interativo:
