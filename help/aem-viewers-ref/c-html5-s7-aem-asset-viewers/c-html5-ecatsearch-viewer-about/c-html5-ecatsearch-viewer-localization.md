---
description: Determinado conteúdo que o eCatalog Viewer exibe está sujeito a localização, incluindo botões de zoom, botões de alteração de página, botão de miniatura, botão de tela cheia, botão de fechamento e botões da barra de rolagem.
solution: Experience Manager
title: Localização dos elementos da interface do usuário
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: c44bfb38-a523-4399-8dbd-936830bb7cac
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1057'
ht-degree: 0%

---

# Localização dos elementos da interface do usuário{#localization-of-user-interface-elements}

Determinado conteúdo que o eCatalog Viewer exibe está sujeito a localização, incluindo botões de zoom, botões de alteração de página, botão de miniatura, botão de tela cheia, botão de fechamento e botões da barra de rolagem.

Todo conteúdo textual no visualizador que pode ser localizado é representado por um identificador especial do SDK do visualizador chamado SYMBOL. Qualquer SYMBOL tem um valor de texto associado ao padrão para a localidade em inglês ( `"en"`) fornecido com o visualizador pronto para uso, e também pode ter valores definidos pelo usuário definidos para quantas localidades forem necessárias.

Quando o visualizador é iniciado, ele verifica o local atual para ver se há um valor definido pelo usuário para cada SYMBOL suportado no local. Se houver, ele usará o valor definido pelo usuário; caso contrário, ele voltará para o texto padrão pronto para uso.

Os dados de localização definidos pelo usuário podem ser passados para o visualizador como um objeto JSON de localização. Esse objeto contém a lista de localidades suportadas, valores de texto SYMBOL para cada localidade e a localidade padrão.

Um exemplo desse objeto de localização:

```
{ 
"en":{ 
"CloseButton.TOOLTIP":"Close", 
"ZoomInButton.TOOLTIP":"Zoom In" 
 }, 
 "fr":{ 
"CloseButton.TOOLTIP":"Fermer", 
"ZoomInButton.TOOLTIP":"Agrandir" 
}, 
defaultLocale:"en" 
}
```

No exemplo acima, o objeto de localização define duas localidades ( `"en"` e `"fr"`) e fornece localização para dois elementos da interface do usuário em cada localidade.

O código da página da Web deve passar esse objeto de localização para o construtor do visualizador como um valor do campo `localizedTexts` do objeto de configuração. Uma opção alternativa é passar o objeto de localização chamando o método `setLocalizedTexts(localizationInfo)`.

Os seguintes SYMBOLs são suportados (supondo que containerId seja a ID do container do visualizador):

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SÍMBOLO </p> </th> 
   <th colname="col2" class="entry"> <p>Dica de ferramenta para... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>Rótulo ARIA para o elemento do visualizador de nível superior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PageView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Descrição da função ARIA para o componente de exibição principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PageView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>Dicas de uso ARIA para usuários de teclado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão Fechar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomInButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão de Mais zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomOutButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão de menos zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomResetButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão de redefinição de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>botão de tela cheia no estado normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>botão de tela cheia no estado de tela cheia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão de rolagem para cima. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão de rolagem para baixo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;ID_contêiner&gt;_rightButton.PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão grande da próxima página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;IDdoContêiner&gt;_leftButton.PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão grande da página anterior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;IDdoContêiner&gt;_lastPageButton.PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão Última página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_secondaryLastPageButton.PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão Última página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;ID_contêiner&gt;_firstPageButton.PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão Primeira página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_secondaryFirstPageButton.PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão Primeira página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;ID_contêiner&gt;_toolBarRightButton.PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão Próxima página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_toolBarLeftButton.PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão da página anterior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ThumbnailPageButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Botão Miniaturas no modo Miniaturas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ThumbnailPageButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Botão Miniaturas no modo normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão Fechar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> InfoPanelPopup.TOOLTIP_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Botão Fechar do Painel Informações. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Ferramenta de compartilhamento social. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão de compartilhamento de email. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Cabeçalho da caixa de diálogo de email. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Botão de fechamento superior direito da caixa de diálogo de email. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.INVALID_ADDRESS </span> </p> </td> 
   <td colname="col2"> <p>Mensagem de erro exibida caso o endereço de email esteja malformado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">CompartilhamentoEmail.PARA </span> </p> </td> 
   <td colname="col2"> <p>Rótulo para o campo de entrada "Para". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ADD </span> </p> </td> 
   <td colname="col2"> <p>Botão Adicionar outro endereço de email. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">CompartilhamentoEmail.ADICIONAR </span> </p> </td> 
   <td colname="col2"> <p>Botão Adicionar outro endereço de email. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">CompartilhamentoEmail.DE </span> </p> </td> 
   <td colname="col2"> <p>Do campo de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.MESSAGE </span> </p> </td> 
   <td colname="col2"> <p>Campo de entrada da mensagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_REMOVE </span> </p> </td> 
   <td colname="col2"> <p>Botão Remover endereço de email. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão Cancelar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Botão Cancelar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão Selecionar tudo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p>Botão Selecionar tudo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão Fechar exibida na parte inferior da caixa de diálogo após o envio do formulário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Botão Fechar exibido na parte inferior da caixa de diálogo após o envio do formulário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão de envio de formulário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p>Botão de envio de formulário. </p> </td> 
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
   <td colname="col2"> <p>Botão Incorporar compartilhamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Cabeçalho da caixa de diálogo Incorporar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Botão de fechamento superior direito da caixa de diálogo Incorporar. </p> </td> 
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
   <td colname="col2"> <p>Legenda do botão Cancelar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Botão Cancelar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CUSTOM_SIZE </span> </p> </td> 
   <td colname="col2"> <p>Texto da última entrada de "tamanho personalizado" na caixa de combinação de tamanho incorporado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão Compartilhar link. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Cabeçalho da caixa de diálogo Vincular. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Botão Fechar da caixa de diálogo de link superior direito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Descrição do link de compartilhamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão Cancelar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Botão Cancelar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão Selecionar tudo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p> Botão Selecionar tudo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão Compartilhar do facebook. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão de compartilhamento do Twitter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão Imprimir. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.HEADER </span> </p> </td> 
   <td colname="col2"> <p>Imprimir cabeçalho da caixa de diálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Caixa de diálogo Imprimir botão Fechar superior direito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE </span> </p> </td> 
   <td colname="col2"> <p>Etiqueta para a seção "Selecionar páginas para impressão". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_CURRENT </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão de opção "Páginas atuais". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_FROM </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão de opção "Espalhar intervalo de". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_TO </span> </p> </td> 
   <td colname="col2"> <p>Legenda para o seletor numérico "para". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_ALL </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão de opção "Todas as páginas". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING </span> </p> </td> 
   <td colname="col2"> <p>Rótulo para a seção "Manuseio de página". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING_ONE </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão de opção "1 página por folha". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING_TWO </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão de opção "2 páginas por folha". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão Cancelar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p> Botão Cancelar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Legenda do botão Enviar para imprimir </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p> Botão Enviar para impressão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FavoritesMenu.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão do menu Favoritos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AddFavoriteButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Botão "Adicionar favorito" no modo Editar favoritos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AddFavoriteButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Botão "Adicionar favorito" no modo normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RemoveFavoriteButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Botão "Remover favorito" no modo Editar favoritos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RemoveFavoriteButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Botão "Remover favorito" no modo normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ViewAllFavoriteButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Botão "Exibir todos os favoritos" quando a exibição Favoritos estiver ativa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ViewAllFavoriteButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Botão "Exibir todos os favoritos" quando a exibição Favoritos estiver inativa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FavoritesEffect.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Ícone de favorito único. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MediaSet.LABEL_XX[_YY] </span> </p> </td> 
   <td colname="col2"> <p>Rótulo da página gerado pelo visualizador no momento do carregamento. </p> <p>O nome desse símbolo é um modelo, onde <span class="codeph"> XX </span> é um índice espelhado de base zero na orientação paisagem, e <span class="codeph"> opcional YY </span> é um índice de página de base zero dentro da página espelhada direcionada por <span class="codeph"> XX </span>. </p> <p>Aplica-se somente ao ativo carregado inicialmente; ignorado se um ativo for alterado usando a chamada de API </span> setAsset() <span class="codeph">. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MediaSet.LABEL_DELIM </span> </p> </td> 
   <td colname="col2"> <p> Caractere usado como delimitador de rótulos de página caso os rótulos sejam definidos para páginas esquerda e direita em uma página espelhada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftRightButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Botão esquerdo de rolagem da barra de controle principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftRightButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Botão de rolagem para a direita da barra de controle principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.PLACEHOLDER </span> </p> </td> 
   <td colname="col2"> <p>O prompt localizado mostrado na caixa de entrada de pesquisa antes que o usuário comece a inserir o texto de pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.INFO_PROMPT </span> </p> </td> 
   <td colname="col2"> <p>Mensagem localizada exibida quando o painel de pesquisa é aberto pela primeira vez, sugerindo que o usuário execute a pesquisa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.INFO_NO_RESULTS </span> </p> </td> 
   <td colname="col2"> <p>Mensagem localizada exibida quando a pesquisa não retornou resultados. </p> <p>Este símbolo oferece suporte ao seguinte token de substituição em tempo de execução: <span class="codeph"> $SEARCH_TEXT$ </span>. O componente o substitui pelo texto de pesquisa inserido pelo usuário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.INFO_RESULTS </span> </p> </td> 
   <td colname="col2"> <p>Mensagem localizada exibida quando a pesquisa for concluída com êxito e retornar pelo menos um resultado. </p> <p>Esse símbolo oferece suporte aos seguintes tokens de substituição em tempo de execução: </p> <p> 
     <ul id="ul_30B76EAB921848069BE843A5F91F697A"> 
      <li id="li_16AF3EFCC4BF4180B66DE5EA82CC77F4"> <span class="codeph"> $SEARCH_TEXT$ </span> - O texto de pesquisa inserido pelo usuário. </li> 
      <li id="li_A0FBF12344B04BF0B702A2B7473330A8"> <span class="codeph"> $HIT_COUNT$ </span> - O número total de ocorrências de pesquisa encontradas. </li> 
      <li id="li_9EB7B41A989B455ABEC72E052284F117"> <span class="codeph"> $PAGE_COUNT$ </span> - O número de páginas do catálogo que contêm pelo menos uma ocorrência de pesquisa. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.THUMBNAIL_LABEL </span> </p> </td> 
   <td colname="col2"> <p>Rótulo localizado para a miniatura de resultados do painel de pesquisa. </p> <p>Esse símbolo oferece suporte aos seguintes tokens de substituição em tempo de execução: </p> <p> 
     <ul id="ul_7620C59FA56544CD9CE9E49B1871BCC1"> 
      <li id="li_FAF092734B4B4B55A309413690DA3FCC"> <span class="codeph"> $PAGE$ </span> - Número da página. </li> 
      <li id="li_3414176505BB4A768FB42341A315E96F"> <span class="codeph"> $PAGE_HIT_COUNT$ </span> - O número de resultados de pesquisa encontrados na página. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.LABEL </span> </p> </td> 
   <td colname="col2"> <p>Define um valor do atributo ARIA </span> aria-label <span class="codeph"> para todo o painel de pesquisa. </p> </td> 
  </tr> 
 </tbody> 
</table>
