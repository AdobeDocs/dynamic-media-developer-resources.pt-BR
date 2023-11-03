---
title: Personalização do visualizador de vídeo de recorte inteligente
description: Personalização do visualizador de vídeo de recorte inteligente
keywords: responsivo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 13a7ced1-0c88-4e56-b46a-08eea7a46a5a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1262'
ht-degree: 0%

---

# Personalização do visualizador de vídeo de recorte inteligente{#customizing-smartcrop-video-viewer}

Todas as personalizações visuais e a maioria das personalizações de comportamento são feitas criando um CSS personalizado.

O fluxo de trabalho sugerido é pegar o arquivo CSS padrão do visualizador apropriado, copiá-lo para um local diferente, personalizá-lo e especificar o local do arquivo personalizado no `style=` comando.

Os arquivos CSS padrão podem ser encontrados no seguinte local:

`<s7_viewers_root>/html5/SmartCropVideoViewer.css`

O arquivo CSS personalizado deve conter as mesmas declarações de classe que a padrão. Se uma declaração de classe for omitida, o visualizador não funcionará corretamente porque não fornecerá estilos padrão internos para elementos da interface do usuário.

Uma maneira alternativa de fornecer regras CSS personalizadas é usar estilos incorporados diretamente na página da Web ou em uma das regras CSS externas vinculadas.

Ao criar CSS personalizado, lembre-se de que o visualizador atribui `.s7smartcropvideoviewer` ao elemento DOM do contêiner. Se você usar um arquivo CSS externo passado com o `style=` comando, use `.s7smartcropvideoviewer` como classe pai no seletor descendente para suas regras CSS. Se você incorporar estilos na página da Web, qualifique também esse seletor com uma ID do elemento DOM do contêiner da seguinte maneira:

`#<containerId>.s7smartcropvideoviewer`

## Criação de CSS responsivo projetado {#section-63e8f93ee2f14fd8bba1ce33a6870b80}

É possível direcionar diferentes dispositivos no CSS para fazer com que o conteúdo seja exibido de forma diferente, dependendo do dispositivo de um usuário. Esse direcionamento inclui, mas não se limita a, diferentes tamanhos de elemento da interface do usuário e resolução do trabalho artístico.

O visualizador suporta dois mecanismos de criação de CSS responsivo projetado: marcadores CSS e consultas de mídia CSS padrão. Você pode usar esses dois mecanismos independentemente ou juntos.

**Marcadores CSS**

Para ajudar a criar CSS projetado de forma responsiva, o visualizador suporta marcadores CSS que classes CSS especiais são atribuídas dinamicamente ao elemento de contêiner do visualizador de nível superior. Esta atribuição é baseada no tamanho do visualizador de tempo de execução e no tipo de entrada usado no dispositivo atual.

O primeiro grupo de marcadores CSS inclui `.s7size_large`, `.s7size_medium`, e `.s7size_small` classes. Elas são aplicadas com base na área de tempo de execução do container do visualizador. Ou seja, se a área do visualizador for igual ou maior que o tamanho de um monitor de desktop comum `.s7size_large` é usada; se a área estiver próxima em tamanho de um dispositivo de tablet comum `.s7size_medium` é atribuído. Para áreas semelhantes a telas de telefones celulares, `.s7size_small` está definido. O principal objetivo desses marcadores CSS é criar diferentes layouts de interface de usuário para telas e tamanhos de visualizador diferentes.

O segundo grupo de marcadores CSS inclui `.s7mouseinput` e `.s7touchinput`. O marcador `.s7touchinput` é definido se o dispositivo atual tiver recursos de entrada de toque; caso contrário, `.s7mouseinput` é usada. Esses marcadores têm como objetivo criar elementos de entrada da interface do usuário com diferentes tamanhos de tela para diferentes tipos de entrada, pois normalmente a entrada por toque requer elementos maiores. Caso o dispositivo tenha recursos de entrada do mouse e de toque, `.s7touchinput` estiver definido e o visualizador renderizar uma interface do usuário amigável para toque.

O CSS de amostra a seguir define o tamanho do botão Reproduzir/pausar para 28 x 28 pixels em sistemas com entrada de mouse e 56 x 56 pixels em dispositivos de toque. Além disso, ele oculta completamente o botão se o tamanho do visualizador se tornar pequeno:

```
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7smartcropvideoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7smartcropvideoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

Para direcionar dispositivos com uma densidade de pixels diferente, use as consultas de mídia CSS. O seguinte bloco de consulta de mídia conteria CSS específico para telas de alta densidade:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

O uso de marcadores CSS é a maneira mais flexível de criar CSS responsivo projetado. Essa flexibilidade permite direcionar não apenas o tamanho da tela do dispositivo, mas o tamanho real do visualizador, que pode ser útil para layouts responsivos de página de design.

Use o arquivo CSS do visualizador padrão como um exemplo de uma abordagem de marcadores CSS.

**Consultas de mídia CSS**

A detecção de dispositivos também pode ser feita usando consultas de mídia CSS pura. Tudo o que está delimitado em um determinado bloco de consulta de mídia é aplicado somente quando é executado em um dispositivo correspondente.

Quando aplicado a Visualizadores móveis, use quatro consultas de mídia CSS, definidas em seu CSS na ordem listada abaixo:

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

Usando a abordagem de consultas de mídia CSS, você deve organizar o CSS com detecção de dispositivo da seguinte maneira:

* Primeiro, a seção específica da área de trabalho define todas as propriedades que são específicas da área de trabalho ou comuns a todas as telas.
* Segundo, as quatro consultas de mídia devem seguir a ordem definida acima e fornecer regras CSS específicas para o tipo de dispositivo correspondente.

Não há necessidade de duplicar todo o CSS do visualizador em cada consulta de mídia. Somente as propriedades específicas de determinados dispositivos são redefinidas em uma consulta de mídia.

## Sprites CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

Muitos elementos da interface do usuário do visualizador são estilizados usando arte-final de bitmap e têm mais de um estado visual distinto. Um bom exemplo é um botão que normalmente tem pelo menos três estados diferentes: &quot;up&quot;, &quot;over&quot; e &quot;down&quot;. Cada estado exige que seu próprio trabalho artístico de bitmap seja atribuído.

Com uma abordagem clássica de estilo, o CSS teria uma referência separada a um arquivo de imagem individual no servidor para cada estado do elemento da interface do usuário. Este é um exemplo de CSS para criar o estilo de um botão de tela cheia:

```
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

A desvantagem dessa abordagem é que o usuário final apresenta oscilação ou atraso na resposta da interface do usuário quando o elemento recebe interação pela primeira vez. Essa ação ocorre porque a arte-final da imagem para o novo estado do elemento ainda não foi baixada. Além disso, essa abordagem pode ter um pequeno impacto negativo no desempenho devido a um aumento no número de chamadas HTTP para o servidor.

Sprites CSS é uma abordagem diferente, onde a arte-final da imagem para todos os estados do elemento é combinada em um único arquivo PNG chamado de &quot;sprite&quot;. Essa &quot;imagem&quot; tem todos os estados visuais para o elemento fornecido posicionados um após o outro. Ao estilizar um elemento de interface do usuário com sprites, a mesma imagem de sprite é referenciada para todos os estados diferentes no CSS. Além disso, a variável `background-position` A propriedade é usada para cada estado para especificar qual parte da imagem &quot;sprite&quot; é usada. Você pode estruturar uma imagem &quot;sprite&quot; de qualquer maneira adequada. Os visualizadores normalmente o empilham verticalmente. Abaixo está um exemplo de &quot;sprite&quot; com o estilo do mesmo botão de tela cheia acima:

```
.s7smartcropvideoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7smartcropvideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## Observações gerais sobre o estilo e conselhos {#section-097418bd618740bba36352629e4d88e1}

* Todos os caminhos para ativos externos no CSS são resolvidos em relação ao local do CSS, não ao local da página do HTML do visualizador. Lembre-se dessa regra ao copiar o CSS padrão para um local diferente. Copie os ativos padrão ou atualize os caminhos no CSS personalizado.
* O formato preferido para arte-final de bitmap é PNG.
* O trabalho artístico de bitmap é atribuído a elementos da interface do usuário usando o `background-image` propriedade.
* A variável `width` e `height` as propriedades de um elemento da interface do usuário definem seu tamanho lógico. O tamanho do bitmap passado para `background-image` não afeta o tamanho lógico.

* Para usar a alta densidade de pixels de telas de alta resolução como o Retina, especifique um trabalho artístico de bitmap duas vezes maior do que o tamanho do elemento da interface de usuário lógica. Em seguida, aplique o `-webkit-background-size:contain` para dimensionar o plano de fundo até o tamanho do elemento da interface lógica.
* Para remover um botão da interface do usuário, adicione `display:none` à sua classe CSS.
* Você pode usar vários formatos para valores de cor compatíveis com CSS. Se precisar de transparência, use o formato `rgba(R,G,B,A)`. Caso contrário, você poderá usar o formato `#RRGGBB`.

* Ao personalizar a interface do usuário do visualizador com CSS, o uso do `!IMPORTANT` a regra não tem suporte para elementos do visualizador de estilos. Em especial, `!IMPORTANT` A regra não deve ser usada para substituir qualquer estilo padrão ou de tempo de execução fornecido pelo visualizador ou pelo SDK do visualizador. O motivo é que isso pode afetar o comportamento dos componentes corretos. Em vez disso, você deve usar seletores de CSS com a especificidade adequada para definir as propriedades de CSS documentadas neste guia de referência.

## Elementos comuns da interface do usuário {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Veja a seguir a documentação de referência dos elementos da interface do usuário que se aplica ao Visualizador de corte inteligente de vídeo:
