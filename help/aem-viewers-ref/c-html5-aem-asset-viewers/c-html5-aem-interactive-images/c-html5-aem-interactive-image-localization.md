---
description: Determinado conteúdo que o Visualizador de Imagem Interativa exibe está sujeito à localização. Isso inclui dicas de ferramentas do elemento da interface do usuário e uma mensagem de informação que é exibida pela exibição de zoom flyout no carregamento.
title: Localização dos elementos da interface do usuário
feature: Dynamic Media Classic,Visualizadores,SDK/API,Imagens interativas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---


# Localização dos elementos da interface do usuário{#localization-of-user-interface-elements}

Determinado conteúdo que o Visualizador de Imagem Interativa exibe está sujeito à localização. Isso inclui dicas de ferramentas do elemento da interface do usuário e uma mensagem de informação que é exibida pela exibição de zoom flyout no carregamento.

Todo conteúdo textual no visualizador que pode ser localizado é representado pelo identificador especial do SDK do visualizador chamado SYMBOL. Qualquer SYMBOL tem um valor de texto associado padrão para uma localidade em inglês ( `"en"`) fornecida com o visualizador pronto para uso e também pode ter valores definidos pelo usuário definidos para quantas localidades forem necessárias.

Quando o visualizador é iniciado, ele verifica o local atual para ver se há um valor definido pelo usuário para cada SYMBOL compatível para esse local. Se houver, ele usará o valor definido pelo usuário; caso contrário, retorna ao texto padrão pronto para uso.

Os dados de localização definidos pelo usuário podem ser passados para o visualizador como um objeto JSON de localização. Esse objeto contém a lista de localidades compatíveis, valores de texto SYMBOL para cada localidade e o local padrão.

Um exemplo desse objeto de localização é o seguinte:

```
{ 
"en":{ 
"Container.LABEL":"Interactive Image Viewer" 
 }, 
 "fr":{ 
"Container.LABEL":"Visionneuse d'images interactive" 
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
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>Descrição da função ARIA para o componente de exibição principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>Dicas de uso de ARIA para usuários de teclado. </p> </td> 
  </tr> 
 </tbody> 
</table>

