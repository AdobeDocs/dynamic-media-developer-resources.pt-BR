---
title: Reprodutor de vídeo
description: O reprodutor de vídeo de recorte inteligente é a área retangular na qual o conteúdo do vídeo é exibido no visualizador.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# Reprodutor de vídeo{#video-player}

O reprodutor de vídeo de recorte inteligente é a área retangular na qual o conteúdo do vídeo é exibido no visualizador.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Se as dimensões do vídeo que está sendo reproduzido não corresponderem às dimensões do reprodutor de vídeo de recorte inteligente, o conteúdo do vídeo será centralizado na área de exibição de retângulo do reprodutor de vídeo de recorte inteligente.

O seguinte seletor de classe CSS controla a aparência do player de vídeo de recorte inteligente:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer
```

**Propriedades CSS do reprodutor de vídeo de recorte inteligente**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo </span> </p> </td> 
   <td colname="col2"> <p>Cor do plano de fundo da exibição principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

A mensagem de erro que é exibida se o sistema não for capaz de reproduzir o vídeo pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obter mais informações.

Exemplo - Para configurar um visualizador de vídeo de recorte inteligente com o tamanho do reprodutor de vídeo de recorte inteligente definido como 512 x 288 pixels.

```
.s7smartcropvideoviewer .s7smartcropvideoplayer{ 
background-color: transparent; 
}
```

As legendas ocultas são colocadas em um contêiner interno dentro do reprodutor de vídeo de recorte inteligente. A posição desse contêiner é controlada por operadores de posicionamento WebVTT compatíveis. O texto da legenda em si está dentro desse contêiner e seu estilo é controlado com o seguinte seletor de classe CSS:

`. s7smartcropvideoviewer .s7videoplayer .s7caption`

**Propriedades CSS de legendas ocultas**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo </span> </p> </td> 
   <td colname="col2"> <p>Plano de fundo do texto da legenda fechada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Fechar cor do texto da legenda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p> Peso da fonte da legenda fechada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte </span> </p> </td> 
   <td colname="col2"> <p> Tamanho da fonte da legenda oculta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes </span> </p> </td> 
   <td colname="col2"> <p>Fonte da legenda oculta. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - Para configurar o texto da legenda fechada para ter 14 pixels, cinza claro, Arial®, em um plano de fundo preto semitransparente:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

A aparência da animação de buffering é controlada com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon
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
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p> Altura do ícone de animação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem esquerda </span> </p> </td> 
   <td colname="col2"> <p> Ícone de animação margem esquerda, normalmente menos metade da largura do ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem superior </span> </p> </td> 
   <td colname="col2"> <p> Margem superior do ícone de animação, normalmente menos a metade da altura do ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p> Arte do botão. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma animação de buffer de 101 pixels de largura, 29 pixels de altura:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
