---
title: Pop-up do painel Informações
description: O pop-up do painel Informações é exibido no meio da área do visualizador quando um usuário ativa um mapa de imagem que tem uma propriedade rollover_key definida no Dynamic Media Classic e se o recurso do painel Informações está configurado corretamente para o visualizador.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: c29f085e-8093-44d2-8f98-9341d780cca8
source-git-commit: 6087b48b898e93e605c3873cbd5132b74d04225f
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# Pop-up do painel Informações{#info-panel-popup}

O pop-up do painel Informações é exibido no meio da área do visualizador quando um usuário ativa um mapa de imagem que tem uma propriedade rollover_key definida no Dynamic Media Classic e se o recurso do painel Informações está configurado corretamente para o visualizador.

O plano de fundo do painel Informações cobre toda a área do visualizador e é controlado com o seguinte seletor de classe CSS:

`.s7ecatalogviewer .s7infopanelpopup .s7backoverlay`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p>Plano de fundo de preenchimento do painel Informações. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - configure o pop-up do painel de informações para usar um plano de fundo preto semitransparente.

```
.s7ecatalogviewer .s7infopanelpopup .s7backoverlay { 
 background-color : rgba(0,0,0,0.75); 
}
```

A caixa de diálogo do painel de informações é exibida por padrão no meio da área do visualizador. No entanto, é possível controlar seu tamanho, alinhamento, plano de fundo e borda com o seletor de classe CSS.

`.s7ecatalogviewer .s7infopanelpopup .s7overlay`

<table id="table_4E666A03A3D44CEEA72225113553AB3F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> saiu de </span> </p> </td> 
   <td colname="col2"> <p>Posição horizontal da caixa de diálogo do painel de informações dentro do preenchimento do plano de fundo do painel da área do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Posição vertical da caixa de diálogo do painel de informações na área do visualizador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura da caixa de diálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do diálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem esquerda </span> </p> </td> 
   <td colname="col2"> <p>Margem esquerda da caixa de diálogo do painel de informações, pode ser usada para fins de centralização. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem superior </span> </p> </td> 
   <td colname="col2"> <p>A margem superior da caixa de diálogo do painel de informações pode ser usada para fins de centralização. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento da caixa de diálogo interna. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>Cor de fundo da caixa de diálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> raio da borda </span> </p> </td> 
   <td colname="col2"> <p>Raio da borda do diálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sombra-caixa </span> </p> </td> 
   <td colname="col2"> <p>Sombra de diálogo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - Para configurar a caixa de diálogo do painel de informações de 300 x 200 pixels que está centralizada na área do visualizador. Ele tem um preenchimento de 40 pixels na parte superior e 10 pixels em todos os outros lados, um plano de fundo cinza-claro e um raio de borda de 10 pixels e sombra.

```
.s7ecatalogviewer .s7infopanelpopup .s7overlay { 
 left: 50%; 
 top: 50%; 
 margin-left: -150px; 
 margin-top: -100px; 
 width: 300px; 
 height: 200px; 
 padding-top: 40px; 
 padding-right: 10px; 
 padding-bottom: 10px; 
 padding-left: 10px; 
 background-color:rgb(221,221,221); 
 border-radius: 10px 10px 10px 10px; 
box-shadow: 0 0 5px rgba(0,0,0,0.25);  
}
```

A caixa de diálogo Painel de informações tem um botão Fechar e clicar ou tocar no botão fecha a caixa de diálogo.

A aparência desse botão é controlada com o seguinte seletor de classe CSS:

`.s7ecatalogviewer .s7infopanelpopup .s7closebutton`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Propriedade CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Posição na borda superior da caixa de diálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> direita </span> </p> </td> 
   <td colname="col2"> <p>Posição da borda direita da caixa de diálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> saiu de </span> </p> </td> 
   <td colname="col2"> <p>Posição da borda esquerda da caixa de diálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> inferior </p> </td> 
   <td colname="col2"> <p>Posição na borda inferior da caixa de diálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p>A imagem exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão oferece suporte ao seletor de atributos `state`, que você pode usar para aplicar capas diferentes a estados de botão diferentes.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - Para configurar um botão Fechar da caixa de diálogo com 28 x 28 pixels e posicionado a 5 pixels da borda superior e direita da caixa de diálogo do painel de informações. Por fim, o exibe uma imagem diferente para cada um dos quatro estados de botão diferentes.

```
.s7ecatalogviewer .s7infopanelpopup .s7closebutton { 
 width: 28px; 
 height: 28px; 
 top: 5px; 
 right: 5px; 
} 
.s7ecatalogviewer .s7infopanelpopup .s7closebutton[state="up"] { 
background-image:url(images/v2/InfoPanelPopup_CloseButton_dark_up.png); 
} 
.s7ecatalogviewer .s7infopanelpopup .s7closebutton[state="over"] { 
background-image:url(images/v2/InfoPanelPopup_CloseButton_dark_over.png); 
} 
.s7ecatalogviewer .s7infopanelpopup .s7closebutton[state="down"] { 
background-image:url(images/v2/InfoPanelPopup_CloseButton_dark_up.png); 
} 
.s7ecatalogviewer .s7infopanelpopup .s7closebutton[state="disabled"] { 
background-image:url(images/v2/InfoPanelPopup_CloseButton_dark_up.png); 
}
```
