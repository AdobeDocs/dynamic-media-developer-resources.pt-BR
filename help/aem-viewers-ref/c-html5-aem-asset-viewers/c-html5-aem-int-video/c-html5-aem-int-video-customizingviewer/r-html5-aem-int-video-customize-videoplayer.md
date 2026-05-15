---
title: Reprodutor de vídeo
description: O reprodutor de vídeo é a área retangular onde o conteúdo do vídeo é exibido no visualizador.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9cfeceff-f6bd-42d9-9b85-456bbaa278fd
TQID: 'https://experienceleague.adobe.com/QE1d7JlPXKNmPNlzSAKTAvBW3xd3m58ITbcIshaqLzQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 307
ht-degree: 0%

---

# Reprodutor de vídeo{#video-player}

O reprodutor de vídeo é a área retangular onde o conteúdo do vídeo é exibido no visualizador.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Se as dimensões do vídeo que está sendo reproduzido não corresponderem às dimensões do reprodutor de vídeo, o conteúdo do vídeo será centralizado na área de exibição retangular do reprodutor de vídeo.

O seletor de classe CSS a seguir controla a aparência do reprodutor de vídeo:

```
.s7interactivevideoviewer .s7videoplayer
```

**Propriedades CSS do reprodutor de vídeo**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>Cor de fundo da janela principal. </p> </td> 
  </tr> 
 </tbody> 
</table>

Você pode localizar a mensagem de erro exibida nos casos em que o sistema não consegue reproduzir o vídeo.

Consulte [Localização de elementos da interface do usuário](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Exemplo - Para configurar um visualizador de vídeo com o tamanho do reprodutor de vídeo definido como 512 x 288 pixels.

```
.s7interactivevideoviewer .s7videoplayer{ 
background-color: transparent; 
}
```

As legendas ocultas são colocadas em um container interno no reprodutor de vídeo. A posição desse contêiner é controlada por operadores de posicionamento WebVTT compatíveis. O texto da legenda em si está dentro desse container, e seu estilo é controlado com o seguinte seletor de classe CSS:

`.s7interactivevideoviewer .s7videoplayer .s7caption`

**Propriedades CSS de legendas ocultas**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>Plano de fundo do texto da legenda oculta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto da legenda oculta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> espessura da fonte </span> </p> </td> 
   <td colname="col2"> <p> Peso da fonte da legenda oculta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte </span> </p> </td> 
   <td colname="col2"> <p> Tamanho da fonte da legenda oculta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Família de fontes <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p>Fonte da legenda oculta. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section-5b82913ff3c44b7b8187969cb15e9560}

Para configurar o texto de legendas ocultas para 14 pixels, cinza claro, Arial®, em um plano de fundo preto semitransparente:

```
.s7interactivevideoviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

A aparência da animação em buffer é controlada com o seguinte seletor de classe CSS:

```
.s7interactivevideoviewer .s7videoplayer .s7waiticon
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
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p> Largura do ícone de animação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p> Altura do ícone de animação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem esquerda </span> </p> </td> 
   <td colname="col2"> <p> Margem esquerda do ícone de animação, normalmente menos metade da largura do ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem superior </span> </p> </td> 
   <td colname="col2"> <p> Margem superior do ícone de animação, normalmente menos metade da altura do ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p> Obstrução de arte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma animação em buffer com 101 pixels de largura e 29 pixels de altura:

```
.s7interactivevideoviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
