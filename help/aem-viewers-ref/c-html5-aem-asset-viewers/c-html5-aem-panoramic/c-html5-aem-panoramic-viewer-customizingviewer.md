---
title: Personalizar visualizador panorâmico
description: Toda personalização visual e a maioria dos comportamentos do Visualizador panorâmico são feitas criando um CSS personalizado.
keywords: responsivo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: c9dda4e8-2781-4870-9ccb-707823c56490
source-git-commit: 7a3ba1cbe063603733a8ff03e8ef1277ec632ec5
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# Personalização do visualizador de vídeo 360{#customizing-video-viewer}

Toda personalização visual e a maioria dos comportamentos são feitos com a criação de um CSS personalizado.

O fluxo de trabalho sugerido é pegar o arquivo CSS padrão para o visualizador apropriado, copiá-lo para um local diferente, personalizá-lo e especificar o local do arquivo personalizado no `style=` comando.

Arquivos CSS padrão podem ser encontrados no seguinte local:

`<s7viewers_root>/html5/PanoramicViewer.css`

O arquivo CSS personalizado deve conter as mesmas declarações de classe que a padrão. Se uma declaração de classe for omitida, o visualizador não funcionará corretamente porque não fornece estilos padrão incorporados para elementos da interface do usuário.

Outra maneira de fornecer regras de CSS personalizadas é usar estilos incorporados diretamente na página da Web ou em uma das regras de CSS externas vinculadas.

Ao criar CSS personalizado, lembre-se de que o visualizador atribui `.s7panoramicviewer` à classe do elemento DOM do contêiner. Se você estiver usando um arquivo CSS externo passado com `style=` , use `.s7panoramicviewer` classe como classe pai no seletor descendente de suas regras CSS. Se você estiver fazendo estilos incorporados na página da Web, qualifique também esse seletor com uma ID do elemento DOM do contêiner da seguinte maneira:

`#<containerId>.s7panoramicviewer.`


## Notas e conselhos gerais sobre estilos {#section-95855dccbbc444e79970f1aaa3260b7b}

* Todos os caminhos para ativos externos dentro do CSS são resolvidos em relação ao local do CSS, não no local da HTML do visualizador. Leve isso em consideração ao copiar o CSS padrão para um local diferente: pode ser necessário copiar os ativos padrão também ou atualizar caminhos no CSS personalizado.
* Você pode usar vários formatos para o valor de cor suportado pelo CSS. Se for necessária transparência, `rgba(R,G,B,A)` é sugerido. Caso contrário, a transparência não é exigida `#RRGGBB` pode ser usada.

Ao personalizar a interface do usuário do visualizador com CSS, o uso de `!IMPORTANT` não há suporte para a regra nos elementos do visualizador de estilo. Em especial, `!IMPORTANT` não deve ser usada para substituir qualquer estilo padrão ou de tempo de execução fornecido pelo visualizador ou pelo SDK do visualizador, pois pode afetar o comportamento correto dos componentes. Em vez disso, seletores de CSS com especificidade adequada devem ser usados para definir propriedades de CSS documentadas neste guia de referência.

## CSS do visualizador panorâmico {#section-9b6d8d601cb441d08214dada7bb4eddc}

**Área do visualizador principal**
A área de visualização principal é a área ocupada pela imagem panorâmica.  Normalmente, ele é configurado para ajustar a tela de dispositivo disponível quando nenhum tamanho é especificado.

A aparência da área de visualização é controlada com o seletor de classe CSS:
`.s7panoramicviewer`

As propriedades CSS aplicáveis incluem:

<table id="table_panA68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> A largura do visualizador; </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> A altura do visualizador; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo: Para configurar um visualizador com tamanho de 1024 x 512 pixels.

```
.s7panoramicviewer {
	width: 1024px;
	height: 500px;	
}
```

**Exibição panorâmica**
A exibição principal consiste na imagem panorâmica.

A aparência da exibição principal é controlada com o seletor de classe CSS:
`.s7panoramicviewer .s7panoramicview`

As propriedades CSS aplicáveis incluem:
<table id="table_pann68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> a cor de fundo da vista principal; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo: Para tornar a exibição principal transparente:

```
.s7panoramicviewer .s7panoramicview {
	background-color: transparent;
}
```
