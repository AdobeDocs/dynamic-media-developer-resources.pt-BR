---
title: Personalização do Visualizador Panorâmico
description: Toda a personalização visual e a maioria das personalizações de comportamento do Visualizador panorâmico é feita por meio da criação de um CSS personalizado.
keywords: responsivo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: c9dda4e8-2781-4870-9ccb-707823c56490
source-git-commit: 7a3ba1cbe063603733a8ff03e8ef1277ec632ec5
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Personalização do visualizador do Video360{#customizing-video-viewer}

Toda a personalização visual e a maioria das personalizações de comportamento são feitas criando um CSS personalizado.

O fluxo de trabalho sugerido é pegar o arquivo CSS padrão do visualizador apropriado, copiá-lo para um local diferente, personalizá-lo e especificar o local do arquivo personalizado no comando `style=`.

Os arquivos CSS padrão podem ser encontrados no seguinte local:

`<s7viewers_root>/html5/PanoramicViewer.css`

O arquivo CSS personalizado deve conter as mesmas declarações de classe que a padrão. Se uma declaração de classe for omitida, o visualizador não funcionará corretamente porque não fornecerá estilos padrão internos para elementos da interface do usuário.

Uma maneira alternativa de fornecer regras CSS personalizadas é usar estilos incorporados diretamente na página da Web ou em uma das regras CSS externas vinculadas.

Ao criar CSS personalizado, lembre-se de que o visualizador atribui a classe `.s7panoramicviewer` ao seu elemento DOM de contêiner. Se você estiver usando um arquivo CSS externo passado com o comando `style=`, use a classe `.s7panoramicviewer` como a classe pai no seletor descendente para suas regras CSS. Se você estiver fazendo estilos incorporados na página da Web, qualifique também esse seletor com uma ID do elemento DOM do contêiner da seguinte maneira:

`#<containerId>.s7panoramicviewer.`


## Observações gerais sobre o estilo e conselhos {#section-95855dccbbc444e79970f1aaa3260b7b}

* Todos os caminhos para ativos externos no CSS são resolvidos em relação ao local do CSS, não ao local da página do HTML do visualizador. Considere isso ao copiar o CSS padrão em um local diferente: pode ser necessário copiar os ativos padrão também ou atualizar caminhos no CSS personalizado.
* Você pode usar vários formatos para valores de cor compatíveis com CSS. Se a transparência for necessária, o formato `rgba(R,G,B,A)` é sugerido. Caso contrário, a transparência não é necessária `#RRGGBB` pode ser usada.

Ao personalizar a interface do usuário do visualizador com CSS, o uso da regra `!IMPORTANT` não tem suporte para elementos do visualizador de estilo. Especificamente, a regra `!IMPORTANT` não deve ser usada para substituir qualquer estilo padrão ou de tempo de execução fornecido pelo visualizador ou pelo SDK do visualizador, pois pode afetar o comportamento adequado dos componentes. Em vez disso, os seletores de CSS com a especificidade adequada devem ser usados para definir as propriedades de CSS documentadas neste guia de referência.

## Visualizador panorâmico CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

**Área do visualizador principal**
A área de visualização principal é a área ocupada pela imagem panorâmica.  Normalmente, ele é configurado para se ajustar à tela do dispositivo disponível quando nenhum tamanho é especificado.

A aparência da área de visualização é controlada com o seletor de classe CSS:
`.s7panoramicviewer`

As propriedades de CSS aplicáveis incluem:

<table id="table_panA68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> a largura do visualizador; </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> a altura do visualizador; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo:
Para configurar um visualizador com tamanho de 1024 x 512 pixels.

```
.s7panoramicviewer {
	width: 1024px;
	height: 500px;	
}
```

**Exibição panorâmica**
A visualização principal consiste na imagem panorâmica.

A aparência da visualização principal é controlada com o seletor de classe CSS:
`.s7panoramicviewer .s7panoramicview`

As propriedades de CSS aplicáveis incluem:
<table id="table_pann68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> a cor de fundo do modo de exibição principal; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo:
Para tornar a exibição principal transparente:

```
.s7panoramicviewer .s7panoramicview {
	background-color: transparent;
}
```
