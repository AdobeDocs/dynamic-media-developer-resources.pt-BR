---
title: Compartilhamento social
description: A ferramenta de compartilhamento em redes sociais aparece no canto superior esquerdo por padrão. Consiste em um botão e um painel que se expande quando o usuário clica ou toca em um botão e contém ferramentas de compartilhamento individuais.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 5cac6c86-08fb-46fd-bab0-ab77154eb770
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# Compartilhamento social{#social-share}

A ferramenta de compartilhamento em redes sociais aparece no canto superior esquerdo por padrão. Consiste em um botão e um painel que se expande quando o usuário clica ou toca em um botão e contém ferramentas de compartilhamento individuais.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A posição e o tamanho da ferramenta de compartilhamento social na interface do usuário do visualizador são controlados com o seguinte:

```
.s7ecatalogsearchviewer .s7socialshare
```

**Propriedades CSS da ferramenta de compartilhamento social**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem superior </span> </p> </td> 
   <td colname="col2"> <p> O deslocamento da parte superior da barra de controle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem=esquerda </span> </p> </td> 
   <td colname="col2"> <p> A distância até o próximo botão à esquerda, ou o lado esquerdo da barra de controle se este botão for o primeiro em uma linha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p> A largura da ferramenta de compartilhamento social. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>A altura da ferramenta de compartilhamento social. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - configure uma ferramenta de compartilhamento em redes sociais posicionada a quatro pixels da parte superior e a cinco pixels da direita do contêiner do visualizador e dimensionada para 28 x 28 pixels.

```
.s7ecatalogsearchviewer .s7socialshare { 
margin-top: 4px; 
margin-left: 10px; width:28px; 
 height:28px; 
}
```

A aparência do botão de ferramenta de compartilhamento em redes sociais é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton
```

**Propriedades CSS do botão de redes sociais**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p> A imagem exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão oferece suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - configure um botão de ferramenta de compartilhamento em redes sociais que exiba uma imagem diferente para cada um dos quatro estados de botão diferentes.

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

A aparência do painel que contém os ícones individuais de compartilhamento em redes sociais é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel
```

**Propriedades CSS do painel de compartilhamento social**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>A cor do plano de fundo do painel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - configurar um painel para ter cor transparente:

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
