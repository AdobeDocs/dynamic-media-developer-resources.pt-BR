---
description: O reprodutor de vídeo é a área retangular na qual o conteúdo de vídeo é exibido no visualizador.
solution: Experience Manager
title: Reprodutor de vídeo
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídia mista
role: Developer,User
exl-id: 2f92d76e-3104-4ad8-9426-662275492251
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# Reprodutor de vídeo{#video-player}

O reprodutor de vídeo é a área retangular na qual o conteúdo de vídeo é exibido no visualizador.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Se as dimensões do vídeo que está sendo reproduzido não corresponderem às dimensões do reprodutor de vídeo, o conteúdo do vídeo será centralizado na área de exibição do retângulo do reprodutor de vídeo.

O seguinte seletor de classe CSS controla a aparência do reprodutor de vídeo:

```
.s7mixedmediaviewer .s7videoplayer
```

**Propriedades CSS do reprodutor de vídeo**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p> A cor de fundo do reprodutor de vídeo. </p> </td> 
  </tr> 
 </tbody> 
</table>

A mensagem de erro que é exibida se o sistema não conseguir reproduzir o vídeo pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) para obter mais informações.

Exemplo - Para tornar o reprodutor de vídeo transparente:

```
.s7mixedmediaviewer .s7videoplayer { 
 background-color: transparent; 
}
```

As legendas são colocadas no contêiner interno no reprodutor de vídeo. A posição desse contêiner é controlada por operadores de posicionamento WebVTT compatíveis. O próprio texto da legenda está dentro desse contêiner; seu estilo é controlado com o seguinte seletor de classe CSS:

```
.s7mixedmediaviewer .s7videoplayer .s7caption
```

**Propriedades CSS de legendas**

<table id="table_5417B0C0343747649502629F43DF231A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>Plano de fundo do texto da legenda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto da legenda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>Espessura da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte  </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Família de fontes. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - Para configurar o texto da legenda para ter 14 pixels de Arial cinza claro em um plano de fundo preto semitransparente:

```
.s7mixedmediaviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

A aparência da animação de buffering é controlada com o seguinte seletor de classe CSS:

```
.s7mixedmediaviewer .s7videoplayer .s7waiticon
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
   <td colname="col2"> <p> Ícone de animação margem esquerda, normalmente menos metade da largura do ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem superior  </span> </p> </td> 
   <td colname="col2"> <p> Margem superior do ícone de animação, normalmente menos a metade da altura do ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Arte do botão. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - Para configurar uma animação de buffer de 101 pixels de largura, 29 pixels de altura:

```
.s7mixedmediaviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
