---
description: Personalização do visualizador de vídeo
keywords: responsive
solution: Experience Manager
title: Personalização do visualizador de vídeo
topic: Dynamic Media
uuid: e18fdf8b-5834-4c99-b8a3-90d1f8310dc1
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '1256'
ht-degree: 0%

---


# Personalização do Visualizador de vídeo{#customizing-video-viewer}

Toda personalização visual e a maioria dos comportamentos são feitos com a criação de um CSS personalizado.

O fluxo de trabalho sugerido é pegar o arquivo CSS padrão para o visualizador apropriado, copiá-lo para um local diferente, personalizá-lo e especificar o local do arquivo personalizado no comando `style=`.

Os arquivos CSS padrão podem ser encontrados no seguinte local:

`<s7_viewers_root>/html5/VideoViewer.css`

O arquivo CSS personalizado deve conter as mesmas declarações de classe que a padrão. Se uma declaração de classe for omitida, o visualizador não funcionará corretamente porque não fornece estilos padrão incorporados para elementos da interface do usuário.

Uma maneira alternativa de fornecer regras CSS personalizadas é usar estilos incorporados diretamente na página da Web ou em uma das regras CSS externas vinculadas.

Ao criar CSS personalizado, lembre-se de que o visualizador atribui a classe `.s7videoviewer` ao elemento DOM do container. Se você usar um arquivo CSS externo transmitido com o comando `style=`, use a classe `.s7videoviewer` como classe pai no seletor descendente para suas regras CSS. Se você incorporar estilos na página da Web, qualifice adicionalmente este seletor com uma ID do elemento DOM do container da seguinte maneira:

`#<containerId>.s7videoviewer`

## Criação de CSS {#section-63e8f93ee2f14fd8bba1ce33a6870b80} projetado responsivo

É possível público alvo de diferentes dispositivos no CSS para fazer com que seu conteúdo seja exibido de forma diferente dependendo do dispositivo do usuário. Essa definição de metas inclui, mas não se limita a, diferentes tamanhos de elementos da interface do usuário e resolução da arte-final.

O visualizador suporta dois mecanismos de criação de CSS responsivo projetado: Marcadores CSS e query de mídia CSS padrão. Você pode usá-los independentemente ou juntos.

**Marcadores CSS**

Para auxiliar na criação de CSS responsivo projetado, o visualizador oferece suporte a marcadores CSS que classes CSS especiais atribuídas dinamicamente ao elemento de container do visualizador de nível superior com base no tamanho do visualizador de tempo de execução e no tipo de entrada usado no dispositivo atual.

O primeiro grupo de marcadores CSS inclui `.s7size_large`, `.s7size_medium` e `.s7size_small` classes. Eles são aplicados com base na área de tempo de execução do container do visualizador. Ou seja, se a área do visualizador for igual ou maior que o tamanho de um monitor de área de trabalho comum `.s7size_large` for usada; se a área estiver próxima em tamanho a um tablet comum `.s7size_medium` for atribuída. Para áreas semelhantes a telas de telefone móvel `.s7size_small` está definido. O objetivo principal desses marcadores CSS é criar diferentes layouts de interface do usuário para telas e tamanhos de visualizador diferentes.

O segundo grupo de marcadores CSS inclui `.s7mouseinput` e `.s7touchinput`. `.s7touchinput` é definido se o dispositivo atual tiver capacidades de entrada de toque; caso contrário,  `.s7mouseinput` será usado. Esses marcadores são destinados a criar elementos de entrada da interface do usuário com tamanhos de tela diferentes para tipos de entrada diferentes, pois normalmente a entrada de toque requer elementos maiores. Se o dispositivo tiver recursos de entrada e toque do mouse, `.s7touchinput` será definido e o visualizador renderizará uma interface de usuário fácil de tocar.

A amostra de CSS a seguir define o tamanho do botão play/pause como 28 x 28 pixels em sistemas com entrada do mouse e 56 x 56 pixels em dispositivos de toque. Além disso, oculta completamente o botão se o tamanho do visualizador se tornar realmente pequeno:

```
.s7videoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7videoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7videoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

Para público alvo de dispositivos com uma densidade de pixels diferente, use query de mídia CSS. O seguinte bloco de query de mídia contém CSS específico para telas de alta densidade:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

O uso de marcadores CSS é a maneira mais flexível de criar um CSS responsivo projetado, pois permite público alvo não apenas do tamanho da tela do dispositivo, mas do tamanho real do visualizador, o que pode ser útil para layouts de página de design responsivos.

Use o arquivo CSS do visualizador padrão como exemplo de uma abordagem de marcadores CSS.

**Query de mídia CSS**

A detecção de dispositivos também pode ser feita usando query de mídia CSS. Tudo o que está incluído em um determinado bloco de query de mídia é aplicado somente quando é executado em um dispositivo correspondente.

Quando aplicado aos Visualizadores móveis, use quatro query de mídia CSS, definidos em seu CSS na ordem listada abaixo:

1. Contém apenas regras específicas para todos os dispositivos de toque.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
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

Usando a abordagem de query de mídia CSS, você deve organizar o CSS com detecção de dispositivos da seguinte maneira:

* Primeiro, a seção específica da área de trabalho define todas as propriedades que são específicas da área de trabalho ou comuns a todas as telas.
* Segundo, os quatro query de mídia devem seguir a ordem definida acima e fornecer regras CSS específicas para o tipo de dispositivo correspondente.

Não há necessidade de duplicado do CSS do visualizador inteiro em cada query de mídia. Somente as propriedades específicas a determinados dispositivos são redefinidas em um query de mídia.

## Sprites CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

Muitos elementos da interface do usuário do visualizador têm estilo usando arte-final bitmap e mais de um estado visual distinto. Um bom exemplo é um botão que normalmente tem pelo menos 3 estados diferentes: &quot;para cima&quot;, &quot;para cima&quot; e &quot;para baixo&quot;. Cada estado requer sua própria arte-final de bitmap atribuída.

Com uma abordagem clássica ao estilo, o CSS teria uma referência separada ao arquivo de imagem individual no servidor para cada estado do elemento da interface do usuário. A seguir está um exemplo de CSS para estilizar um botão de tela cheia:

```
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

A desvantagem dessa abordagem é que o usuário final sofre oscilações ou retardamento da resposta da interface do usuário quando o elemento é interagido pela primeira vez. Essa ação ocorre porque a arte-final da imagem para o novo estado do elemento ainda não foi baixada. Além disso, essa abordagem pode ter um impacto negativo no desempenho devido ao aumento no número de chamadas HTTP para o servidor.

Os sprites CSS são uma abordagem diferente na qual a arte-final de imagem para todos os estados do elemento é combinada em um único arquivo PNG chamado de &quot;sprite&quot;. Tal &quot;sprite&quot; tem todos os estados visuais para um determinado elemento posicionado um após o outro. Ao estilizar um elemento da interface do usuário com sprites, a mesma imagem de sprite é referenciada para todos os estados diferentes no CSS. Além disso, a propriedade `background-position` é usada para cada estado para especificar qual parte da imagem &quot;sprite&quot; é usada. Você pode estruturar uma imagem &quot;sprite&quot; de qualquer maneira adequada. Os visualizadores normalmente o têm empilhado verticalmente. Abaixo está um exemplo baseado em &quot;sprite&quot; de como estilizar o mesmo botão de tela inteira da parte superior:

```
.s7videoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## Notas e conselhos gerais sobre estilo {#section-097418bd618740bba36352629e4d88e1}

* Todos os caminhos para ativos externos dentro do CSS são resolvidos em relação ao local do CSS e não ao local da página HTML do visualizador. Lembre-se de levar essa regra em conta ao copiar o CSS padrão para um local diferente. Copie os ativos padrão ou os caminhos de atualização no CSS personalizado.
* O formato preferido para a arte-final bitmap é PNG.
* A arte-final bitmap é atribuída aos elementos da interface do usuário usando a propriedade `background-image`.
* As propriedades `width` e `height` de um elemento da interface do usuário definem seu tamanho lógico. O tamanho do bitmap passado para `background-image` não afeta o tamanho lógico.

* Para usar a alta densidade de pixels de telas de alta resolução, como Retina, especifique a arte-final bitmap duas vezes maior que o tamanho do elemento lógico da interface do usuário. Em seguida, aplique a propriedade `-webkit-background-size:contain` para dimensionar o plano de fundo para baixo no tamanho do elemento da interface do usuário lógica.
* Para remover um botão da interface do usuário, adicione `display:none` à sua classe CSS.
* Você pode usar vários formatos para valores de cor compatíveis com CSS. Se precisar de transparência, use o formato `rgba(R,G,B,A)`. Caso contrário, você pode usar o formato `#RRGGBB`.

* Ao personalizar a interface do usuário do visualizador com CSS, o uso da regra `!IMPORTANT` não é compatível com elementos do visualizador de estilo. Especificamente, a regra `!IMPORTANT` não deve ser usada para substituir qualquer estilo padrão ou de tempo de execução fornecido pelo visualizador ou pelo SDK do visualizador. Isso pode afetar o comportamento dos componentes apropriados. Em vez disso, você deve usar seletores de CSS com a especificidade adequada para definir as propriedades de CSS documentadas neste guia de referência.

## Elementos Comuns da Interface do Usuário {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

A seguir estão os elementos da interface do usuário que fazem referência à documentação que se aplica ao Visualizador de vídeo:
