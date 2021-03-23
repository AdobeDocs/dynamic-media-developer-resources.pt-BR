---
description: Determinado conteúdo exibido pelo Visualizador de carrossel está sujeito à localização. Isso inclui botões de navegação de slides.
seo-description: Determinado conteúdo exibido pelo Visualizador de carrossel está sujeito à localização. Isso inclui botões de navegação de slides.
seo-title: Localização dos elementos da interface do usuário
solution: Experience Manager
title: Localização dos elementos da interface do usuário
uuid: 82e4dc72-cc12-4ab5-8370-6270f9a3d45f
feature: Dynamic Media Classic,Visualizadores,SDK/API,Banners em carrossel
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---


# Localização dos elementos da interface do usuário{#localization-of-user-interface-elements}

Determinado conteúdo exibido pelo Visualizador de carrossel está sujeito à localização. Isso inclui botões de navegação de slides.

Todo conteúdo textual no visualizador que pode ser localizado é representado pelo identificador especial do SDK do visualizador chamado SYMBOL. Qualquer SYMBOL tem um valor de texto associado padrão para uma localidade em inglês ( `"en"`) fornecida com o visualizador pronto para uso e também pode ter valores definidos pelo usuário definidos para quantas localidades forem necessárias.

Quando o visualizador é iniciado, ele verifica o local atual para ver se há um valor definido pelo usuário para cada SYMBOL compatível para esse local. Se houver, ele usará o valor definido pelo usuário; caso contrário, retorna ao texto padrão pronto para uso.

Os dados de localização definidos pelo usuário podem ser passados para o visualizador como um objeto JSON de localização. Esse objeto contém a lista de localidades compatíveis, valores de texto SYMBOL para cada localidade e o local padrão.

Um exemplo desse objeto de localização é o seguinte:

```
{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left", 
"PanRightButton.TOOLTIP":"Right" 
 }, 
 "fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste", 
"PanRightButton .TOOLTIP":"Droit" 
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
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Estado do botão de pausa de reprodução selecionado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Estado do botão de pausa de reprodução não selecionado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CAROUSELVIEWER_TOOLTIP_GOTO  </span> </p> </td> 
   <td colname="col2"> <p> Dica de ferramenta e rótulo ARIA para botões de slide anteriores e seguintes. </p> <p>Aceita dois tokens de substituição: <span class="codeph"> $CURRENT_FRAME$ </span> para o índice de slide atual e <span class="codeph"> $TOTAL_FRAMES$ </span> para o número total de slides. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p> Rótulo ARIA para o elemento do visualizador de nível superior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p> Descrição da função ARIA para o componente de exibição principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p> Dicas de uso de ARIA para usuários de teclado. </p> </td> 
  </tr> 
 </tbody> 
</table>

