---
title: Localização dos elementos da interface do usuário
description: Determinados conteúdos exibidos pelo Visualizador de corte inteligente de vídeo estão sujeitos a localização. Esse conteúdo inclui dicas de ferramentas do elemento da interface do usuário e uma mensagem de erro que é exibida quando o vídeo não pode ser reproduzido.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: e5019948-d8ed-4bb2-b652-2936b6f694c9
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# Localização dos elementos da interface do usuário{#localization-of-user-interface-elements}

Determinados conteúdos exibidos pelo Visualizador de corte inteligente de vídeo estão sujeitos a localização. Esse conteúdo inclui dicas de ferramentas do elemento da interface do usuário e uma mensagem de erro que é exibida quando o vídeo não pode ser reproduzido.

Todo conteúdo textual no visualizador que pode ser localizado é representado por um identificador SDK especial do visualizador chamado SYMBOL. Qualquer SYMBOL tem um valor de texto associado ao padrão para a localidade em inglês ( `"en"`) fornecido com o visualizador pronto para uso. Ela também pode ter valores definidos pelo usuário definidos para quantas localidades forem necessárias.

Quando o visualizador é iniciado, ele verifica o local atual para ver se há um valor definido pelo usuário para cada SYMBOL suportado para o local. Se houver, ele usará o valor definido pelo usuário; caso contrário, ele voltará para o texto padrão pronto para uso.

Os dados de localização definidos pelo usuário podem ser passados para o visualizador como um objeto JSON de localização. Esse objeto contém a lista de localidades suportadas, valores de texto SYMBOL para cada localidade e a localidade padrão.

Um exemplo desse objeto de localização é o seguinte:

```
{ 
"en":{ 
"SmartCropVideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Play" 
 }, 
 "fr":{ 
"SmartCropVideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Jouer" 
}, 
defaultLocale:"en" 
}
```

No exemplo acima, o objeto de localização define duas localidades ( `"en"` e `"fr"`) e fornece localização para dois elementos de interface do usuário em cada localidade.

O código da página da Web deve passar esse objeto de localização para o construtor do visualizador como um valor do campo `localizedTexts` do objeto de configuração. Uma opção alternativa é passar o objeto de localização chamando o método `setLocalizedTexts(localizationInfo)`.

Os seguintes SYMBOLs são suportados:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SÍMBOLO </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p> Rótulo ARIA para o elemento do visualizador de nível superior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELETED </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o estado do botão pausar reprodução selecionado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o estado do botão Pausar reprodução desmarcado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_REPLAY </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o estado do botão Reproduzir pausa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoScrubber.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o depurador de vídeo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoTime.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o tempo de vídeo na barra de controle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o estado de volume mutável selecionado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o volume mutável desmarcado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_VOLUME </span> </p> </td> 
   <td colname="col2"> <p> Rótulo do botão deslizante de volume exposto por meio do atributo ARIA <span class="codeph"> aria-valuetext </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o estado de botão de tela inteira selecionado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o estado de botão em tela cheia desmarcado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o estado de botão de legenda oculta selecionado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o estado de botão de legenda oculta desmarcado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para a ferramenta de compartilhamento em redes sociais. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o botão de compartilhamento de email. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o cabeçalho da caixa de diálogo de email. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o botão de fechamento superior direito da caixa de diálogo de email. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.INVALID_ADDRESS </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para a mensagem de erro exibida caso o endereço de email esteja malformado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">CompartilhamentoEmail.PARA </span> </p> </td> 
   <td colname="col2"> <p>Rótulo para o campo de entrada "Para". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ADD </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o botão "Adicionar outro endereço de email". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">CompartilhamentoEmail.ADICIONAR </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão "Adicionar outro endereço de email". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">CompartilhamentoEmail.DE </span> </p> </td> 
   <td colname="col2"> <p>Rótulo para o campo de entrada "De". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.MESSAGE </span> </p> </td> 
   <td colname="col2"> <p>Rótulo para o campo de entrada "Mensagem". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_REMOVE </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o botão "Remover endereço de email". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão "Cancelar". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o botão "Cancelar". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão Fechar exibida na parte inferior da caixa de diálogo após o envio do formulário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o botão Fechar exibido na parte inferior da caixa de diálogo após o envio do formulário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão de envio de formulário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o botão de envio de formulário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_SUCCESS </span> </p> </td> 
   <td colname="col2"> <p>Mensagem de confirmação exibida quando o email foi enviado com êxito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CompartilhamentoEmail.ENVIAR_FALHA </span> </p> </td> 
   <td colname="col2"> <p>Mensagem de erro exibida quando o email não foi enviado com êxito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o botão incorporar compartilhamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o cabeçalho da caixa de diálogo incorporada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o botão de fechamento superior direito da caixa de diálogo incorporada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Descrição do texto do código incorporado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.EMBED_SIZE </span> </p> </td> 
   <td colname="col2"> <p>Rótulo para a caixa de combinação de tamanho incorporado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão "Cancelar". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o botão "Cancelar". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão "Selecionar tudo". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AÇÃO EmbedShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o botão "Selecionar tudo". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CUSTOM_SIZE </span> </p> </td> 
   <td colname="col2"> <p>Texto da última entrada de "tamanho personalizado" na caixa de combinação de tamanho incorporado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o botão de compartilhamento de link. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o cabeçalho da caixa de diálogo do link. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o botão de fechamento superior direito da caixa de diálogo de link. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Descrição do link de compartilhamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão "Cancelar". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o botão "Cancelar". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão "Selecionar tudo". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AÇÃO LinkShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o botão "Selecionar tudo". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o botão Compartilhar do Facebook. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o botão de compartilhamento do Twitter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SmartCropVideoPlayer.ERROR </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para a mensagem de erro que é exibida quando não é possível reproduzir o vídeo. </p> </td> 
  </tr> 
 </tbody> 
</table>
