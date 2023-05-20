---
title: Localização dos elementos da interface do usuário
description: Determinado conteúdo que o Visualizador de imagem suspensa exibe está sujeito a localização. Esse conteúdo inclui dicas de ferramentas do elemento da interface do usuário e mensagens de informações exibidas pela exibição de zoom de imagem suspensa ao carregar.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 49795aa1-07c7-4f2e-bfd9-51d6581898ed
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Localização dos elementos da interface do usuário{#localization-of-user-interface-elements}

Determinado conteúdo que o Visualizador de imagem suspensa exibe está sujeito a localização. Esse conteúdo inclui dicas de ferramentas do elemento da interface do usuário e mensagens de informações exibidas pela exibição de zoom de imagem suspensa ao carregar.

Todo conteúdo textual no visualizador que pode ser localizado é representado pelo identificador especial do SDK do visualizador chamado SYMBOL. Qualquer SÍMBOLO tem um valor de texto associado padrão para um local em inglês ( `"en"`) fornecidos com o visualizador pronto para uso e também podem ter valores definidos pelo usuário definidos para quantas localidades forem necessárias.

Quando o visualizador é iniciado, ele verifica o local atual para ver se há um valor definido pelo usuário para cada SYMBOL compatível para esse local. Se houver, ele usará o valor definido pelo usuário; caso contrário, ele voltará para o texto padrão pronto para uso.

Os dados de localização definidos pelo usuário podem ser passados para o visualizador como um objeto JSON de localização. Esse objeto contém a lista de localidades suportadas, valores de texto SYMBOL para cada localidade e a localidade padrão.

Um exemplo desse objeto de localização é o seguinte:

```
{ 
"en":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Tap and hold to zoom" 
 }, 
 "fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Appuyez et maintenez pour agrandir" 
}, 
defaultLocale:"en" 
}
```

No exemplo acima, o objeto de localização define dois locais ( `"en"` e `"fr"`) e fornece localização para dois elementos da interface do usuário em cada local.

O código da página da Web deve passar esse objeto de localização para o construtor do visualizador, como um valor de `localizedTexts` do objeto de configuração. Uma opção alternativa é passar o objeto de localização chamando o `setLocalizedTexts(localizationInfo)` método.

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
   <td colname="col1"> <p> <span class="codeph"> RÓTULO.Contêiner </span> </p> </td> 
   <td colname="col2"> <p>Rótulo ARIA para o elemento do visualizador de nível superior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Descrição da função ARIA para o componente de exibição principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>Dicas de uso ARIA para usuários de teclado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_OVER </span> </p> </td> 
   <td colname="col2"> <p>Mensagem de informação para sistemas desktop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_TAP </span> </p> </td> 
   <td colname="col2"> <p>Mensagem de informação para dispositivos sensíveis ao toque. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta do botão de rolagem para a esquerda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta do botão de rolagem para a direita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> BotãoDeRolagemParaCima.DICADEFERRAMENTA </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta para o botão de rolagem para cima. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Dica de ferramenta do botão de rolagem para baixo. </p> </td> 
  </tr> 
 </tbody> 
</table>
