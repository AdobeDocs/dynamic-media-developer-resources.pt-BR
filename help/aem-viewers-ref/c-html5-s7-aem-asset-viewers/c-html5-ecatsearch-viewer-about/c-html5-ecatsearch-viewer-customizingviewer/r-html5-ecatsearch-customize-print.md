---
title: Imprimir
description: A ferramenta Imprimir consiste em um botão adicionado à barra de controle e à caixa de diálogo modal exibida quando a ferramenta é ativada.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: c5939cdc-fa4e-4f19-b2a9-21b389492c4f
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '1488'
ht-degree: 0%

---

# Imprimir{#print}

A ferramenta Imprimir consiste em um botão adicionado à barra de controle e à caixa de diálogo modal exibida quando a ferramenta é ativada.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A aparência do botão de impressão é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7print
```

**Propriedades CSS do botão de impressão**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem superior </span> </p> </td> 
   <td colname="col2"> <p> O deslocamento da parte superior da barra de controle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem esquerda </span> </p> </td> 
   <td colname="col2"> <p> A distância até o próximo botão à esquerda, ou o lado esquerdo da barra de controle se este botão for o primeiro em uma linha. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
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
>Esse botão oferece suporte ao `state` seletor de atributo, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - Para configurar um botão de impressão com 28 x 28 pixels e exibir uma imagem diferente para cada um dos quatro estados de botão diferentes.

```
.s7ecatalogsearchviewer .s7print { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7print[state='up'] { 
background-image:url(images/v2/Print_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7print[state='over'] { 
background-image:url(images/v2/Print_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7print[state='down'] { 
background-image:url(images/v2/Print_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7print[state='disabled'] { 
background-image:url(images/v2/Print_dark_disabled.png); 
}
```

A sobreposição de plano de fundo que cobre a página da Web quando a caixa de diálogo está ativa é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay
```

**Propriedades CSS da sobreposição inversa**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidade </span> </p> </td> 
   <td colname="col2"> <p> Opacidade de sobreposição de plano de fundo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Cor de sobreposição do plano de fundo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar a sobreposição do plano de fundo como cinza com 70% de opacidade:

```
.s7ecatalogsearchviewer .s7printdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Por padrão, a caixa de diálogo modal é exibida centralizada na tela em sistemas desktop. O posicionamento e o dimensionamento da caixa de diálogo são gerenciados pelo componente. A caixa de diálogo é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7kprintdialog .s7dialog
```

**Propriedades CSS da caixa de diálogo**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Raio da borda da caixa de diálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Cor de fundo da caixa de diálogo; </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - Para configurar uma caixa de diálogo com um plano de fundo cinza:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialog { 
background-color: #dddddd; 
}
```

O cabeçalho da caixa de diálogo consiste em um ícone, um texto de título e um botão Fechar. O contêiner de cabeçalho é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader
```

**Propriedades CSS do cabeçalho da caixa de diálogo**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p> Preenchimento interno para conteúdo de cabeçalho. </p> </td> 
  </tr> 
 </tbody> 
</table>

O ícone e o texto do título são colocados em um container extra controlado com o seguinte:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader .s7dialogline
```

**Propriedades CSS da linha de diálogo**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p> Preenchimento interno para o ícone e título do cabeçalho. </p> </td> 
  </tr> 
 </tbody> 
</table>

O ícone de cabeçalho é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadericon
```

**Propriedades CSS do ícone de cabeçalho da caixa de diálogo**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Imagem do ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

O título do cabeçalho é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadertext
```

**Propriedades CSS do texto do cabeçalho da caixa de diálogo**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Peso da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Altura da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Família da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento de texto interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

O botão Fechar é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7closebutton
```

**Propriedades CSS do botão Fechar **

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Posição vertical do botão em relação ao contêiner de cabeçalho. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> direita </span> </p> </td> 
   <td colname="col2"> <p> Posição do botão horizontal em relação ao contêiner de cabeçalho. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Imagem do botão para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esse botão oferece suporte ao `state` seletor de atributo, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

A dica de ferramenta do botão Fechar e o título da caixa de diálogo podem ser localizados. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - Para configurar o cabeçalho da caixa de diálogo com preenchimento, ícone de 22 x 22 pixels e um título de 16 pontos em negrito. E, finalmente, um botão Fechar de 28 x 28 pixels posicionado a dois pixels da parte superior e a dois pixels da direita do contêiner da caixa de diálogo:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgprint_cap.png"); 
    height: 22px; 
    width: 22px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogsearchviewer .s7printdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

O rodapé da caixa de diálogo consiste nos botões Cancelar e Enviar para Impressão. O contêiner de rodapé é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter
```

**Propriedades CSS do rodapé da caixa de diálogo **

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borda </span> </p> </td> 
   <td colname="col2"> <p> Borda que você pode usar para separar visualmente o rodapé do restante da caixa de diálogo. </p> </td> 
  </tr> 
 </tbody> 
</table>

O rodapé tem um contêiner interno que mantém ambos os botões. Ele é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbuttoncontainer
```

**Propriedades CSS do contêiner de botão da caixa de diálogo**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p> Preenchimento interno entre o rodapé e os botões. </p> </td> 
  </tr> 
 </tbody> 
</table>

O botão Cancelar é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton
```

**Propriedades CSS do botão Cancelar da caixa de diálogo**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p> Cor do texto do botão para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo do botão para cada estado. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esse botão oferece suporte ao `state` seletor de atributo, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

O botão Enviar para impressão é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton
```

**Propriedades CSS do botão de ação da caixa de diálogo**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p> Cor do texto do botão para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo do botão para cada estado. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esse botão oferece suporte ao `state` seletor de atributo, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

Além disso, ambos os botões compartilham uma classe CSS comum, que pode conter configurações CSS que são as mesmas para outros botões da caixa de diálogo:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter .s7button
```

**Propriedades CSS do botão**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Peso da fonte do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Família de fontes do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura da linha </span> </p> </td> 
   <td colname="col2"> <p> Altura do texto dentro do botão. Afeta o alinhamento vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow </span> </p> </td> 
   <td colname="col2"> <p>Sombra projetada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem direita </span> </p> </td> 
   <td colname="col2"> <p>Margem direita do botão. </p> </td> 
  </tr> 
 </tbody> 
</table>

As dicas de ferramentas do botão podem ser localizadas. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - Para configurar um rodapé de caixa de diálogo com o botão Cancelar 64 x 34 e um botão Enviar para Impressão 96 x 34, com a cor do texto e a cor do plano de fundo diferentes para cada estado do botão:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton { 
 width:96px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

A área principal da caixa de diálogo, entre o cabeçalho e o rodapé, contém conteúdo da caixa de diálogo. Em todos os casos, o componente gerencia a largura dessa área. Não é possível defini-la no CSS. A área de diálogo principal é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea
```

**Propriedades CSS da área de exibição da caixa de diálogo **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p> A altura da área da caixa de diálogo principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>A cor de fundo da área da caixa de diálogo principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem </span> </p> </td> 
   <td colname="col2"> <p>Margem externa. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - Para configurar uma área de diálogo principal para ter uma altura calculada automaticamente, ter uma margem de dez pixels e usar um plano de fundo branco:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:auto; 
}
```

Todo o conteúdo do formulário (como rótulos e campos de entrada) reside dentro de um container controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody
```

**Propriedades CSS do corpo da caixa de diálogo **

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - Para configurar o conteúdo do formulário para ter um preenchimento de dez pixels:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogbody { 
    padding: 10px; 
}
```

O formulário da caixa de diálogo é preenchido linha por linha, onde cada linha carrega uma parte do conteúdo do formulário (como um rótulo e um campo de entrada de texto). A linha de formulário única é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline
```

**Propriedades CSS da linha da caixa de diálogo**

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento de linha interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - Para configurar um formulário de caixa de diálogo com preenchimento de dez pixels para cada linha:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

O tamanho do bloco de conteúdo da caixa de diálogo é controlado com o seguinte seletor de classe CSS:

```
 .s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide
```

**Propriedades CSS da largura de entrada da caixa de diálogo**

<table id="table_FFF0B02B564C443CA8713103D723C733"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do bloco. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento de linha interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir um bloco de conteúdo com 430 pixels de largura e 10 pixels de preenchimento na parte inferior:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

Todos os rótulos estáticos no formulário da caixa de diálogo são controlados com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel
```

Essa classe não é adequada para controlar o tamanho ou a posição do rótulo porque você pode aplicá-la a textos em vários locais na interface do usuário do formulário.

**Propriedades CSS do rótulo da caixa de diálogo. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Espessura da fonte do rótulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte do rótulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Família de fontes do rótulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto do rótulo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Os rótulos da caixa de diálogo podem ser localizados. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - para configurar todos os rótulos para serem cinza, negrito, com uma fonte de nove pixels:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

Os controles de entrada são colocados no container e controlados com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer
```

**Propriedades CSS do container de entrada da caixa de diálogo**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento à esquerda </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir um preenchimento de 30 pixels a partir da borda esquerda da caixa de diálogo.

```
.s7ecatalogsearchviewer .s7printdialog .s7dialoginputcontainer { 
    padding-left: 30px; 
}
```

Os botões de opção e seu texto de legenda são controlados com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption
```

**Propriedades CSS da opção de caixa de diálogo**

<table id="table_3B4D85C5A0254A17A34D57F84F8200F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p> A largura total do botão de opção com uma legenda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto da legenda. </p> </td> 
  </tr> 
 </tbody> 
</table>

O espaçamento entre o botão de opção e sua legenda é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoptioninput
```

**Propriedades CSS da entrada de opção da caixa de diálogo**

<table id="table_BDD03247E594416D93CDF8604DCE937B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem direita </span> </p> </td> 
   <td colname="col2"> <p> Espaçamento entre o botão de opção e sua legenda. </p> </td> 
  </tr> 
 </tbody> 
</table>

Os seletores numéricos para a seleção do intervalo de impressão são controlados com o seguinte seletor de classe CSS

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogrange
```

**Propriedades CSS do intervalo de impressão da caixa de diálogo**

<table id="table_35413C16F6B840EBBEEA17890F2A0490"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p> Largura do seletor numérico. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem </span> </p> </td> 
   <td colname="col2"> <p> Espaçamento ao redor do seletor numérico. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar todos os botões de opção para ter 150 pixels de largura com texto preto, espaçamento de dez pixels e seletores numéricos de 42 pixels de largura:

```
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption { 
    color: #000000; 
    width: 150px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogoption input { 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7printdialog .s7dialogrange { 
    margin-left: 10px; 
    margin-right: 10px; 
    width: 42px; 
}
```

O divisor horizontal entre a seleção de intervalo de páginas e as seções de layout de impressão é controlado com o seguinte seletor de classe CSS:

```
 .s7ecatalogsearchviewer 
.s7printdialog .s7horizontaldivider
```

**Propriedades CSS do divisor horizontal**

<table id="table_AB42F1DC92BB4946868F0A9FE86ABAA6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borda </span> </p> </td> 
   <td colname="col2"> <p> Borda ao redor do divisor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do divisor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem </span> </p> </td> 
   <td colname="col2"> <p>Margem externa </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um divisor cinza de 430 pixels de largura com um preenchimento vertical de 10 pixels em ambos os lados e uma margem de dez pixels na parte superior:

```
.s7ecatalogsearchviewer .s7printdialog .s7horizontaldivider { 
    border-top: 1px solid #aaaaaa; 
    margin-top: 10px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 430px; 
}
```
