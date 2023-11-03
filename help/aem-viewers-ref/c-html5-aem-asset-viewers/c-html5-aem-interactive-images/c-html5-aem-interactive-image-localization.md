---
title: Localização dos elementos da interface do usuário
description: Determinados conteúdos exibidos pelo Visualizador de imagens interativas estão sujeitos a localização. Esse conteúdo inclui dicas de ferramentas do elemento da interface do usuário e uma mensagem de informação exibida pela exibição de zoom de imagem suspensa ao carregar.
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 19749c74-5c31-4dcf-ab07-0e7f10176a86
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Localização dos elementos da interface do usuário{#localization-of-user-interface-elements}

Determinados conteúdos exibidos pelo Visualizador de imagens interativas estão sujeitos a localização. Esse conteúdo inclui dicas de ferramentas do elemento da interface do usuário e uma mensagem de informação exibida pela exibição de zoom de imagem suspensa ao carregar.

Todo conteúdo textual no visualizador que pode ser localizado é representado pelo identificador especial do SDK do visualizador chamado SYMBOL. Qualquer SÍMBOLO tem um valor de texto associado ao padrão para um local em inglês ( `"en"`) fornecido com o visualizador pronto para uso e pode ter valores definidos pelo usuário definidos para quantas localidades forem necessárias.

Quando o visualizador é iniciado, ele verifica o local atual para ver se há um valor definido pelo usuário para cada SYMBOL compatível para esse local. Se houver, ele usará o valor definido pelo usuário; caso contrário, ele voltará para o texto padrão pronto para uso.

Os dados de localização definidos pelo usuário podem ser passados para o visualizador como um objeto JSON de localização. Esse objeto contém a lista de localidades suportadas, valores de texto SYMBOL para cada localidade e a localidade padrão.

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

No exemplo acima, o objeto de localização define dois locais ( `"en"` e `"fr"`) e fornece localização para dois elementos da interface do usuário em cada local.

O código da página da Web deve passar o objeto de localização para o construtor do visualizador, como um valor de `localizedTexts` do objeto de configuração. Uma opção alternativa é passar o objeto de localização chamando `setLocalizedTexts(localizationInfo)` método.

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
   <td colname="col1"> <p> <span class="codeph"> RÓTULO.Contêiner </span> </p> </td> 
   <td colname="col2"> <p>Rótulo ARIA para o elemento do visualizador de nível superior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Descrição da função ARIA para o componente de exibição principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>Dicas de uso ARIA para usuários de teclado. </p> </td> 
  </tr> 
 </tbody> 
</table>
