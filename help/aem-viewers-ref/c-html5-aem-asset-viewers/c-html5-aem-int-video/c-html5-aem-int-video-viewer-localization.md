---
description: Determinado conteúdo que o Visualizador de vídeo interativo exibe está sujeito à localização. Isso inclui dicas de ferramentas do elemento da interface do usuário e uma mensagem de erro que é exibida quando o vídeo não pode ser reproduzido.
seo-description: Determinado conteúdo que o Visualizador de vídeo interativo exibe está sujeito à localização. Isso inclui dicas de ferramentas do elemento da interface do usuário e uma mensagem de erro que é exibida quando o vídeo não pode ser reproduzido.
seo-title: Localização dos elementos da interface do usuário
solution: Experience Manager
title: Localização dos elementos da interface do usuário
uuid: 7c880e25-76dc-43d3-83fc-12de92afd35f
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interativos
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 0%

---


# Localização dos elementos da interface do usuário{#localization-of-user-interface-elements}

Determinado conteúdo que o Visualizador de vídeo interativo exibe está sujeito à localização. Isso inclui dicas de ferramentas do elemento da interface do usuário e uma mensagem de erro que é exibida quando o vídeo não pode ser reproduzido.

Todo conteúdo textual no visualizador que pode ser localizado é representado pelo identificador especial do SDK do visualizador chamado SYMBOL. Qualquer SYMBOL tem um valor de texto associado padrão para uma localidade em inglês ( `"en"`) fornecida com o visualizador pronto para uso e também pode ter valores definidos pelo usuário definidos para quantas localidades forem necessárias.

Quando o visualizador é iniciado, ele verifica o local atual para ver se há um valor definido pelo usuário para cada SYMBOL compatível para esse local. Se houver, ele usará o valor definido pelo usuário; caso contrário, retorna ao texto padrão pronto para uso.

Os dados de localização definidos pelo usuário podem ser passados para o visualizador como um objeto JSON de localização. Esse objeto contém a lista de localidades compatíveis, valores de texto SYMBOL para cada localidade e o local padrão.

Um exemplo desse objeto de localização é o seguinte:

```
{ 
"en":{ 
"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Play" 
 }, 
 "fr":{ 
"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Jouer" 
}, 
defaultLocale:"en" 
}
```

No exemplo acima, o objeto de localização define duas localidades ( `"en"` e `"fr"`) e fornece a localização de dois elementos da interface do usuário em cada localidade.

O código da página da Web deve passar o objeto de localização para o construtor do visualizador, como um valor do campo `localizedTexts` do objeto de configuração. Uma opção alternativa é passar o objeto de localização chamando o método `setLocalizedTexts(localizationInfo)`.

Os seguintes SYMBOLs são suportados:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SÍMBOLO </p> </th> 
   <th colname="col2" class="entry"> <p>Dica de ferramenta para... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>Rótulo ARIA para o elemento do visualizador de nível superior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p> Estado do botão de pausa de reprodução selecionado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Estado do botão de pausa de reprodução desmarcado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_REPLAY  </span> </p> </td> 
   <td colname="col2"> <p> Reproduzir estado do botão de pausa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoScrubber.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Limpador de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoTime.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Tempo do vídeo na barra de controle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p> Volume mutável selecionado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Volume mutável desmarcado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_VOLUME  </span> </p> </td> 
   <td colname="col2"> <p> Rótulo do botão deslizante do volume exposto por meio do atributo ARIA <span class="codeph"> aria-value </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Botão de tela cheia em estado normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Botão de tela cheia no estado de tela cheia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p> Estado do botão de legenda fechada selecionado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p> Estado do botão de legenda fechada desmarcado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> InterativeSwatches.BANNER  </span> </p> </td> 
   <td colname="col2"> <p>Legenda do banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botão Rolar para cima. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botão Rolar para baixo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Ferramenta de compartilhamento em redes sociais. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botão Compartilhar link. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>Cabeçalho da caixa de diálogo Link. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>Botão Fechar superior direito da caixa de diálogo Link. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>Descrição do link de compartilhamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão Cancelar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Botão Cancelar . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão Selecionar tudo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_ACTION  </span> </p> </td> 
   <td colname="col2"> <p> Selecione o botão All . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botão Compartilhar do Facebook. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Botão Compartilhar do Twitter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Chame para o botão Fechar do painel de ação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoPlayer.ERROR  </span> </p> </td> 
   <td colname="col2"> <p>Mensagem de erro que é exibida quando nenhuma reprodução de vídeo é possível. </p> </td> 
  </tr> 
 </tbody> 
</table>

