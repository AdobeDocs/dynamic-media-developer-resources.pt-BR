---
description: Determinado conteúdo exibido pelo Visualizador de rotação está sujeito a localização, incluindo botões de zoom e um botão de tela cheia.
seo-description: Determinado conteúdo exibido pelo Visualizador de rotação está sujeito a localização, incluindo botões de zoom e um botão de tela cheia.
seo-title: Localização dos elementos da interface do usuário
solution: Experience Manager
title: Localização dos elementos da interface do usuário
topic: Dynamic media
uuid: bf38bdef-a31f-4f2f-a8f5-3d3d4eac95ab
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Localização dos elementos da interface do usuário{#localization-of-user-interface-elements}

Determinado conteúdo exibido pelo Visualizador de rotação está sujeito a localização, incluindo botões de zoom e um botão de tela cheia.

Todo conteúdo textual no visualizador que pode ser localizado é representado por um identificador especial do SDK do visualizador chamado SYMBOL. Qualquer SYMBOL tem um valor de texto associado padrão para a localidade em inglês ( `"en"`) fornecida com o visualizador predefinido. Também pode ter valores definidos pelo usuário definidos para tantas localidades quantas forem necessárias.

Quando o visualizador é start, ele verifica a localidade atual para ver se há um valor definido pelo usuário para cada SYMBOL suportado para a localidade. Se houver, ele usará o valor definido pelo usuário; caso contrário, ele voltará para o texto padrão predefinido.

Os dados de localização definidos pelo usuário podem ser passados para o visualizador como um objeto JSON de localização. Esse objeto contém a lista de localidades suportadas, os valores de texto SYMBOL para cada localidade e a localidade padrão.

Um exemplo desse objeto de localização é o seguinte:

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

No exemplo acima, o objeto localização define duas localidades ( `"en"` e `"fr"`) e fornece localização para dois elementos da interface do usuário em cada localidade.

O código da página da Web deve passar o objeto de localização para o construtor do visualizador, como um valor do `localizedTexts` campo do objeto de configuração. Uma opção alternativa é passar o objeto de localização chamando o `setLocalizedTexts(localizationInfo)` método.

Os seguintes SYMBOLs são suportados:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SÍMBOLO </p> </th> 
   <th colname="col2" class="entry"> <p>Dica de ferramenta para o... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.RÓTULO </span> </p> </td> 
   <td colname="col2"> <p>Rótulo ARIA para elemento visualizador de nível superior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SpinView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Descrição da função ARIA para o componente principal da visualização. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SpinView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>Dicas de uso ARIA para usuários de teclado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão Fechar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomInButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão Mais zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomOutButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão Menos zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomResetButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Botão de redefinição de zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Botão de tela inteira em estado normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Botão de tela cheia no estado de tela cheia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Gire o botão esquerdo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Gire o botão direito. </p> </td> 
  </tr> 
 </tbody> 
</table>

