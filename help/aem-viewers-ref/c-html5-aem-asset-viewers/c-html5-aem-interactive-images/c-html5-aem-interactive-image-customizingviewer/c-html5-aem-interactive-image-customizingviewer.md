---
title: Personalização do Visualizador de imagens interativo
description: Toda a personalização visual e a maioria das personalizações de comportamento do Visualizador de imagem interativo é feita criando um CSS personalizado.
keywords: responsivo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: bb3cfe4a-ec60-4c10-82fe-9e4f8f7c586f
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '1287'
ht-degree: 0%

---

# Personalização do Visualizador de imagens interativo{#customizing-interactive-image-viewer}

Toda a personalização visual e a maioria das personalizações de comportamento do Visualizador de imagem interativo é feita criando um CSS personalizado.

O fluxo de trabalho sugerido é pegar o arquivo CSS padrão do visualizador apropriado, copiá-lo para um local diferente, personalizá-lo e especificar o local do arquivo personalizado no comando `style=`.

Os arquivos CSS padrão podem ser encontrados no seguinte local:

`<s7viewers_root>/etc/dam/viewers/s7viewers/html5/InteractiveImage.css`

O arquivo CSS personalizado deve conter as mesmas declarações de classe que a padrão. Se uma declaração de classe for omitida, o visualizador não funcionará corretamente porque não fornecerá estilos padrão internos para elementos da interface do usuário.

Uma maneira alternativa de fornecer regras CSS personalizadas é usar estilos incorporados diretamente na página da Web ou em uma das regras CSS externas vinculadas.

Ao criar CSS personalizado, lembre-se de que o visualizador atribui a classe `.s7interactiveimage` ao seu elemento DOM de contêiner. Se você estiver usando um arquivo CSS externo passado com o comando `style=`, use a classe `.s7interactiveimage` como a classe pai no seletor descendente para suas regras CSS. Se você estiver adicionando estilos incorporados na página da Web, qualifique também esse seletor com uma ID do elemento DOM do contêiner da seguinte maneira:

`#<containerId>.s7interactiveimage`

## Criação de CSS responsivo projetado {#section-0bb49aca42d242d9b01879d5ba59d33b}

É possível direcionar diferentes dispositivos e tamanhos de incorporação no CSS para fazer com que o conteúdo seja exibido de forma diferente, dependendo do dispositivo de um usuário ou de um layout de página da Web específico. Essa técnica inclui, mas não se limita a, layouts diferentes, tamanhos de elemento da interface do usuário e resolução do trabalho artístico.

O visualizador suporta dois mecanismos de criação de CSS responsivo projetado: marcadores CSS e consultas de mídia CSS padrão. É possível usar esses marcadores ou consultas independentemente ou juntos.

**marcadores CSS**

Para ajudar a criar CSS projetado e responsivo, o visualizador é compatível com marcadores CSS. Esses marcadores são classes CSS especiais atribuídas dinamicamente ao elemento de contêiner do visualizador de nível superior. Elas se baseiam no tamanho do visualizador de tempo de execução e no tipo de entrada usado no dispositivo atual.

O primeiro grupo de marcadores CSS contém classes `.s7size_large`, `.s7size_medium` e `.s7size_small`. Elas são aplicadas com base na área de tempo de execução do container do visualizador. Por exemplo, se a área do visualizador for igual ou maior que o tamanho de um monitor de desktop comum, use `.s7size_large`. Se a área estiver próxima a um dispositivo tablet comum, atribua `.s7size_medium`. Para áreas semelhantes a telas de telefones celulares, use o `.s7size_small`. O principal objetivo desses marcadores CSS é criar diferentes layouts de interface de usuário para telas e tamanhos de visualizador diferentes.

O segundo grupo de marcadores CSS contém `.s7mouseinput` e `.s7touchinput`. O marcador CSS `.s7touchinput` será definido se o dispositivo atual tiver entrada por toque. Caso contrário, `.s7mouseinput` será usado. Esses marcadores têm como objetivo criar elementos de entrada da interface do usuário com diferentes tamanhos de tela para diferentes tipos de entrada, pois normalmente a entrada por toque requer elementos maiores.

O exemplo de CSS a seguir define o tamanho do botão de ampliação para 28 x 28 pixels em sistemas com entrada de mouse e para 56 x 56 pixels em dispositivos de entrada de toque. Se o visualizador for dimensionado ainda menor, ele será definido como 20 x 20 pixels.

```
.s7interactiveimage.s7mouseinput .s7imagemapeffect .s7icon { 
    width:28px; 
    height:28px; 
} 
.s7interactiveimage.s7touchinput .s7imagemapeffect .s7icon { 
    width:56px; 
    height:56px; 
} 
.s7interactiveimage.s7size_small .s7imagemapeffect .s7icon { 
    width:20px; 
    height:20px; 
}
```

Para direcionar dispositivos com diferentes densidades de pixel, você deve usar consultas de mídia CSS. O seguinte bloco de consulta de mídia conteria CSS específico para telas de alta densidade:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

O uso de marcadores CSS é a maneira mais flexível de criar CSS projetado responsivo, pois permite direcionar não apenas o tamanho da tela do dispositivo, mas o tamanho real do visualizador, o que é útil para layouts de design responsivos.

Você pode usar o arquivo CSS do visualizador padrão como exemplo de uma abordagem de marcadores CSS.

**Consultas de mídia CSS**

Também é possível realizar a detecção de dispositivos usando consultas de mídia CSS puras. Tudo o que está delimitado em um determinado bloco de consulta de mídia é aplicado somente quando é executado em um dispositivo correspondente.

Quando aplicado a Visualizadores móveis, use quatro consultas de mídia CSS, definidas em seu CSS, na ordem listada abaixo:

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

* Primeiro, a seção específica da área de trabalho define todas as propriedades que são específicas da área de trabalho ou comuns a todas as telas.
* E, em segundo lugar, as quatro consultas de mídia vão na ordem definida acima e fornecem regras CSS específicas para o tipo de dispositivo correspondente.

Não há necessidade de duplicar todo o CSS do visualizador em cada consulta de mídia. Somente as propriedades específicas de determinados dispositivos são redefinidas em uma consulta de mídia.

## sprites CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

Muitos elementos da interface do usuário do visualizador são estilizados usando arte-final de bitmap e têm mais de um estado visual distinto. Um bom exemplo é um botão que normalmente tem pelo menos três estados diferentes: `up`, `over` e `down`. Cada estado exige que seu próprio trabalho artístico de bitmap seja atribuído.

Com uma abordagem clássica de estilo, o CSS teria uma referência separada ao arquivo de imagem individual no servidor para cada estado do elemento da interface do usuário. Este é um exemplo de CSS para criar o estilo de um botão de zoom:

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

A desvantagem dessa abordagem é que o usuário final apresenta oscilação ou atraso na resposta da interface do usuário quando o elemento recebe interação pela primeira vez. Essa ação ocorre porque a arte-final da imagem para o novo estado do elemento ainda não foi baixada. Além disso, essa abordagem pode ter um pequeno impacto negativo no desempenho devido a um aumento no número de chamadas HTTP para o servidor.

Sprites CSS é uma abordagem diferente, onde a arte-final da imagem para todos os estados do elemento é combinada em um único arquivo PNG chamado de &quot;sprite&quot;. Essa &quot;imagem&quot; tem todos os estados visuais para o elemento fornecido posicionados um após o outro. Ao estilizar um elemento de interface do usuário com sprites, a mesma imagem de sprite é referenciada para todos os estados diferentes no CSS. Além disso, a propriedade `background-position` é usada para cada estado para especificar qual parte da imagem &quot;sprite&quot; é usada. Você pode estruturar uma imagem &quot;sprite&quot; de qualquer maneira adequada. Os visualizadores normalmente o empilham verticalmente.

Veja a seguir um exemplo do estilo &quot;sprite&quot; do mesmo botão de aumento:

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
background-position: -0px -56px; width: 56px; height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
background-position: -0px -0px; width: 56px; height: 56px; 
}
```

## Observações gerais sobre o estilo e conselhos {#section-95855dccbbc444e79970f1aaa3260b7b}

* Ao personalizar a interface do usuário do visualizador com CSS, o uso da regra `!IMPORTANT` não tem suporte para elementos do visualizador de estilo. Especificamente, a regra `!IMPORTANT` não deve ser usada para substituir qualquer estilo padrão ou de tempo de execução fornecido pelo visualizador ou pelo SDK do visualizador. O motivo para isso é que pode afetar o comportamento dos componentes corretos. Em vez disso, você deve usar seletores de CSS com a especificidade adequada para definir as propriedades de CSS documentadas neste guia de Referência de visualizadores.
* Todos os caminhos para ativos externos no CSS são resolvidos em relação ao local do CSS, não ao local da página do HTML do visualizador. Esteja ciente dessa regra ao copiar o CSS padrão para um local diferente. Copie os ativos padrão ou atualize todos os caminhos no CSS personalizado.
* O formato preferido para arte-final de bitmap é PNG.
* O trabalho artístico de bitmap é atribuído a elementos da interface do usuário usando a propriedade `background-image`.
* As propriedades `width` e `height` de um elemento da interface do usuário definem seu tamanho lógico. O tamanho do bitmap passado para `background-image` não afeta seu tamanho lógico.
* Para usar a alta densidade de pixels de telas de alta resolução como o Retina, especifique um trabalho artístico de bitmap duas vezes maior do que o tamanho do elemento da interface de usuário lógica. Em seguida, aplique a propriedade `-webkit-background-size:contain` para dimensionar o plano de fundo até o tamanho do elemento da interface de usuário lógica.
* Para remover um botão da interface do usuário, adicione `display:none` à classe CSS.
* Você pode usar vários formatos para valores de cor compatíveis com CSS. Se precisar de transparência, use o formato `rgba(R,G,B,A)`. Caso contrário, você pode usar o formato `#RRGGBB`.

## Elementos comuns da interface do usuário {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Veja a seguir a documentação de referência dos elementos da interface do usuário que se aplica ao Visualizador de imagem de vídeo:
