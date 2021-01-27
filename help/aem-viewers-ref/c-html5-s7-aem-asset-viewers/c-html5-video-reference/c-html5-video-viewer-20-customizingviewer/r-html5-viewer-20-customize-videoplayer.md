---
description: O player de vídeo é a área retangular na qual o conteúdo do vídeo é exibido no visualizador.
seo-description: O player de vídeo é a área retangular na qual o conteúdo do vídeo é exibido no visualizador.
seo-title: Reprodutor de vídeo
solution: Experience Manager
title: Reprodutor de vídeo
topic: Dynamic Media
uuid: 2748c3d3-b974-4e54-8218-a2ec9e31a668
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---


# Reprodutor de vídeo{#video-player}

O player de vídeo é a área retangular na qual o conteúdo do vídeo é exibido no visualizador.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Se as dimensões do vídeo que está sendo reproduzido não corresponderem às dimensões do player de vídeo, o conteúdo do vídeo será centralizado na área de exibição do retângulo do player de vídeo.

O seletor de classe CSS a seguir controla a aparência do player de vídeo:

```
.s7videoviewer .s7videoplayer
```

**Propriedades de CSS do player de vídeo**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor do plano de fundo da visualização principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

A mensagem de erro que é exibida se o sistema não for capaz de reproduzir o vídeo pode ser localizada. Consulte [Localização de elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obter mais informações.

Exemplo - Para configurar um visualizador de vídeo com o tamanho do player de vídeo definido como 512 x 288 pixels.

```
.s7videoviewer .s7videoplayer{ 
background-color: transparent; 
}
```

As legendas ocultas são colocadas em um container interno dentro do player de vídeo. A posição desse container é controlada pelos operadores de posicionamento WebVTT suportados. O próprio texto da legenda está dentro desse container e seu estilo é controlado com o seguinte seletor de classe CSS:

`. s7videoviewer .s7 videoplayer .s7caption`

**Propriedades de CSS de legendas ocultas**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Plano de fundo do texto da legenda fechada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor  </span> </p> </td> 
   <td colname="col2"> <p>Fechar a cor do texto da legenda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-peso  </span> </p> </td> 
   <td colname="col2"> <p> Peso de fonte de legenda fechada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p> Tamanho da fonte da legenda fechada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Fonte da legenda fechada. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - Para configurar o texto da legenda para 14 pixels, cinza claro, Arial, em um plano de fundo preto semitransparente:

```
.s7videoviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

A aparência da animação de buffering é controlada com o seguinte seletor de classe CSS:

```
.s7videoviewer .s7videoplayer .s7waiticon
```

**Propriedades CSS do ícone de espera**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Largura do ícone de animação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p> Altura do ícone de animação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem esquerda  </span> </p> </td> 
   <td colname="col2"> <p> Margem esquerda do ícone Animação, normalmente menos metade da largura do ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem superior  </span> </p> </td> 
   <td colname="col2"> <p> Margem superior do ícone de animação, normalmente menos metade da altura do ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Nódulo de arte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma animação de buffering para ter 101 pixels de largura, 29 pixels de altura:

```
.s7videoviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```

