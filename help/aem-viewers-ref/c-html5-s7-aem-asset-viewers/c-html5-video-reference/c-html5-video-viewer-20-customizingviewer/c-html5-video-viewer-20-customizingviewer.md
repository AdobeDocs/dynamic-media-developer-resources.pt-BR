---
description: Personalizar visualizador de vídeo
keywords: responsivo
solution: Experience Manager
title: Personalizar visualizador de vídeo
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '1267'
ht-degree: 0%

---


# Personalizar visualizador de vídeo{#customizing-video-viewer}

Toda personalização visual e a maioria dos comportamentos são feitos com a criação de um CSS personalizado.

O fluxo de trabalho sugerido é pegar o arquivo CSS padrão do visualizador apropriado, copiá-lo para um local diferente, personalizá-lo e especificar o local do arquivo personalizado no comando `style=`.

Arquivos CSS padrão podem ser encontrados no seguinte local:

`<s7_viewers_root>/html5/VideoViewer.css`

O arquivo CSS personalizado deve conter as mesmas declarações de classe que a padrão. Se uma declaração de classe for omitida, o visualizador não funcionará corretamente porque não fornece estilos padrão incorporados para elementos da interface do usuário.

Uma maneira alternativa de fornecer regras de CSS personalizadas é usar estilos incorporados diretamente na página da Web ou em uma das regras de CSS externas vinculadas.

Ao criar CSS personalizado, lembre-se de que o visualizador atribui a classe `.s7videoviewer` ao elemento DOM do contêiner. Se você usar um arquivo CSS externo passado com o comando `style=`, use a classe `.s7videoviewer` como classe pai no seletor descendente para suas regras CSS. Se você incorporar estilos na página da Web, qualifique também esse seletor com uma ID do elemento DOM do contêiner da seguinte maneira:

`#<containerId>.s7videoviewer`

## Criando CSS responsivo projetado {#section-63e8f93ee2f14fd8bba1ce33a6870b80}

É possível direcionar diferentes dispositivos no CSS para fazer com que o conteúdo seja exibido de forma diferente, dependendo do dispositivo de um usuário. Esse direcionamento inclui, mas não se limita a, diferentes tamanhos de elementos da interface do usuário e resolução do trabalho artístico.

O visualizador aceita dois mecanismos para criar CSS responsivo projetado: Marcadores CSS e consultas de mídia CSS padrão. Você pode usá-los independentemente ou juntos.

**Marcadores CSS**

Para auxiliar na criação de CSS responsivo projetado, o visualizador aceita marcadores CSS que possuem classes CSS especiais atribuídas dinamicamente ao elemento do contêiner do visualizador de nível superior com base no tamanho do visualizador de tempo de execução e no tipo de entrada usado no dispositivo atual.

O primeiro grupo de marcadores CSS inclui `.s7size_large`, `.s7size_medium` e `.s7size_small` classes. Eles são aplicados com base na área de tempo de execução do contêiner do visualizador. Ou seja, se a área do visualizador for igual ou maior que o tamanho de um monitor de desktop comum `.s7size_large` for usado; se a área estiver próxima em tamanho de um tablet comum, `.s7size_medium` será atribuído. Para áreas semelhantes a telas de celular, `.s7size_small` está definido. O objetivo principal desses marcadores CSS é criar diferentes layouts de interface do usuário para diferentes telas e tamanhos de visualizador.

O segundo grupo de marcadores CSS inclui `.s7mouseinput` e `.s7touchinput`. `.s7touchinput` é definido se o dispositivo atual tiver recursos de entrada por toque; caso contrário,  `.s7mouseinput` será usado. Esses marcadores são destinados a criar elementos de entrada da interface do usuário com tamanhos de tela diferentes para tipos de entrada diferentes, pois normalmente a entrada por toque requer elementos maiores. Caso o dispositivo tenha recursos de entrada e toque do mouse, `.s7touchinput` é definido e o visualizador renderiza uma interface de usuário fácil de tocar.

A amostra de CSS a seguir define o tamanho do botão reproduzir/pausar como 28 x 28 pixels em sistemas com entrada de mouse e 56 x 56 pixels em dispositivos de toque. Além disso, ele oculta completamente o botão se o tamanho do visualizador se tornar realmente pequeno:

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

Para direcionar dispositivos com uma densidade de pixels diferente, use consultas de mídia CSS. O seguinte bloco de consulta de mídia contém CSS específico para telas de alta densidade:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

Usar marcadores CSS é a maneira mais flexível de criar CSS projetado responsivo, pois permite direcionar não apenas o tamanho da tela do dispositivo, mas o tamanho real do visualizador, o que pode ser útil para layouts de página de design responsivo.

Use o arquivo CSS do visualizador padrão como exemplo de uma abordagem de marcadores CSS.

**Consultas de mídia CSS**

A detecção de dispositivo também pode ser feita usando queries de mídia CSS puras. Tudo que é delimitado em um determinado bloco de consulta de mídia é aplicado somente quando é executado em um dispositivo correspondente.

Quando aplicado a visualizadores móveis, use quatro consultas de mídia CSS, definidas em seu CSS na ordem listada abaixo:

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

* Primeiro, a seção específica do desktop define todas as propriedades que são específicas do desktop ou comuns a todas as telas.
* Em segundo lugar, as quatro consultas de mídia devem ir na ordem definida acima e fornecer regras de CSS específicas para o tipo de dispositivo correspondente.

Não há necessidade de duplicar todo o CSS do visualizador em cada consulta de mídia. Somente as propriedades específicas de determinados dispositivos são redefinidas em uma consulta de mídia.

## Sprites CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

Muitos elementos da interface do usuário do visualizador são estilizados usando a arte-final de bitmap e têm mais de um estado visual distinto. Um bom exemplo é um botão que normalmente tem pelo menos 3 estados diferentes: &quot;para cima&quot;, &quot;para cima&quot; e &quot;para baixo&quot;. Cada estado requer sua própria arte bitmap atribuída.

Com uma abordagem clássica ao estilo, o CSS teria uma referência separada para o arquivo de imagem individual no servidor para cada estado do elemento da interface do usuário. Veja a seguir um exemplo de CSS para criar estilo em um botão de tela cheia:

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

A desvantagem dessa abordagem é que o usuário final apresenta cintilação ou resposta retardada da interface do usuário quando o elemento interagiu pela primeira vez. Essa ação ocorre porque a arte-final da imagem do novo estado do elemento ainda não foi baixada. Além disso, essa abordagem pode ter um impacto negativo no desempenho devido ao aumento do número de chamadas HTTP para o servidor.

Os sprites CSS são uma abordagem diferente, na qual a arte-final de imagem de todos os estados do elemento é combinada em um único arquivo PNG chamado de &quot;sprite&quot;. Esse &quot;sprite&quot; tem todos os estados visuais para o determinado elemento posicionado um após o outro. Ao estilizar um elemento da interface do usuário com sprites, a mesma imagem de sprite é referenciada para todos os estados diferentes no CSS. Além disso, a propriedade `background-position` é usada para cada estado para especificar qual parte da imagem &quot;sprite&quot; é usada. Você pode estruturar uma imagem &quot;sprite&quot; de qualquer maneira adequada. Os visualizadores normalmente o têm empilhado verticalmente. Abaixo está um exemplo baseado em &quot;sprite&quot; de colocar o mesmo botão de tela cheia acima:

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

* Todos os caminhos para ativos externos dentro do CSS são resolvidos em relação ao local do CSS, não no local da página HTML do visualizador. Lembre-se de levar essa regra em conta ao copiar o CSS padrão para um local diferente. Copie os ativos padrão ou atualize caminhos no CSS personalizado.
* O formato preferido para a arte-final de bitmap é PNG.
* A arte-final do bitmap é atribuída aos elementos da interface do usuário usando a propriedade `background-image` .
* As propriedades `width` e `height` de um elemento da interface do usuário definem o tamanho lógico. O tamanho do bitmap passado para `background-image` não afeta o tamanho lógico.

* Para usar a alta densidade de pixels de telas de alta resolução como Retina, especifique a arte-final de bitmap duas vezes maior que o tamanho do elemento da interface de usuário lógica. Em seguida, aplique a propriedade `-webkit-background-size:contain` para dimensionar o plano de fundo para baixo no tamanho do elemento da interface do usuário lógica.
* Para remover um botão da interface do usuário, adicione `display:none` a sua classe CSS.
* Você pode usar vários formatos para o valor de cor que o CSS suporta. Se precisar de transparência, use o formato `rgba(R,G,B,A)`. Caso contrário, você poderá usar o formato `#RRGGBB`.

* Ao personalizar a interface do usuário do visualizador com CSS, o uso da regra `!IMPORTANT` não é compatível com os elementos do visualizador de estilo. Especificamente, a regra `!IMPORTANT` não deve ser usada para substituir qualquer estilo padrão ou de tempo de execução fornecido pelo visualizador ou pelo SDK do visualizador. Isso pode afetar o comportamento de componentes adequados. Em vez disso, você deve usar seletores de CSS com a especificidade adequada para definir propriedades de CSS documentadas neste guia de referência.

## Elementos Comuns Da Interface Do Usuário {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Veja a seguir a documentação de referência dos elementos da interface do usuário que se aplica ao Visualizador de vídeo:
