---
title: Compartilhamento de email
description: A ferramenta Compartilhamento de email consiste em um botão adicionado ao painel Compartilhamento em redes sociais e à caixa de diálogo modal que é exibida quando a ferramenta é ativada. A posição do botão é totalmente gerenciada pela ferramenta Compartilhamento em redes sociais.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 4c72500b-9750-4fae-9447-96cf600b31c7
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '3081'
ht-degree: 0%

---

# Compartilhamento de email{#email-share}

A ferramenta Compartilhamento de email consiste em um botão adicionado ao painel Compartilhamento em redes sociais e à caixa de diálogo modal que é exibida quando a ferramenta é ativada. A posição do botão é totalmente gerenciada pela ferramenta Compartilhamento em redes sociais.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A aparência do botão de compartilhamento de email é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emailshare
```

**Propriedades CSS da ferramenta de compartilhamento de email**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
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
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p> A imagem exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão oferece suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

É possível remover o botão do painel Compartilhamento em redes sociais definindo a propriedade CSS `display:none` em sua classe CSS.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - Para configurar um botão de compartilhamento de email com 28 x 28 pixels e exibir uma imagem diferente para cada um dos quatro estados de botão diferentes.

```
.s7ecatalogviewer .s7emailshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7emailshare[state='up'] { 
background-image:url(images/v2/EmailShare_dark_up.png); 
} 
.s7ecatalogviewer .s7emailshare[state='over'] { 
background-image:url(images/v2/EmailShare_dark_over.png); 
} 
.s7ecatalogviewer .s7emailshare[state='down'] { 
background-image:url(images/v2/EmailShare_dark_down.png); 
} 
.s7ecatalogviewer .s7emailshare[state='disabled'] { 
background-image:url(images/v2/EmailShare_dark_disabled.png); 
}
```

A sobreposição de plano de fundo que cobre a página da Web quando a caixa de diálogo está ativa é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7backoverlay
```

**Propriedades CSS da sobreposição inversa**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidade </span> </p> </td> 
   <td colname="col2"> <p> Opacidade de sobreposição de plano de fundo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>Cor de sobreposição do plano de fundo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar a sobreposição do plano de fundo como cinza com 70% de opacidade:

```
.s7ecatalogviewer .s7emaildialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Por padrão, a caixa de diálogo modal é exibida centralizada na tela em sistemas desktop e ocupa toda a área da página da Web em dispositivos de toque. Em todos os casos, o posicionamento e o dimensionamento da caixa de diálogo são gerenciados pelo componente. A caixa de diálogo é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialog
```

**Propriedades CSS da caixa de diálogo**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> raio da borda </span> </p> </td> 
   <td colname="col2"> <p> Raio da borda da caixa de diálogo (caso a caixa de diálogo não use toda a janela do navegador); </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p> Cor de fundo da caixa de diálogo; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p> Deve ser desdefinido ou definido como 100%, nesse caso, a caixa de diálogo usa toda a janela do navegador (esse modo é preferível em dispositivos de toque); </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p> Deve ser desdefinido ou definido como 100%, nesse caso, a caixa de diálogo usa toda a janela do navegador (esse modo é preferível em dispositivos de toque). </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar a caixa de diálogo para usar toda a janela do navegador e ter um fundo branco em dispositivos de toque:

```
.s7ecatalogviewer .s7touchinput .s7emaildialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

O cabeçalho da caixa de diálogo consiste em um ícone, um texto de título e um botão Fechar. O contêiner de cabeçalho é controlado com o seguinte seletor de classe CSS

```
.s7ecatalogviewer .s7emaildialog .s7dialogheader
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

O ícone e o texto do título são colocados em um container extra controlado com

```
.s7ecatalogviewer .s7emaildialog .s7dialogheader .s7dialogline
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
.s7ecatalogviewer .s7emaildialog .s7dialogheadericon
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
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p>Imagem do ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

O título do cabeçalho é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogheadertext
```

**Propriedades CSS do texto do cabeçalho da caixa de diálogo**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> espessura da fonte </span> </p> </td> 
   <td colname="col2"> <p>Peso da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte </span> </p> </td> 
   <td colname="col2"> <p>Altura da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Família de fontes <span class="codeph"> </span> </p> </td> 
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
.s7ecatalogviewer .s7emaildialog .s7closebutton
```

**Propriedades CSS do botão Fechar &#x200B;**

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
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p>Imagem do botão para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão oferece suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

A dica de ferramenta do botão Fechar e o título da caixa de diálogo podem ser localizados. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - Para configurar o cabeçalho da caixa de diálogo com preenchimento, ícone de 24 x 17 pixels e um título de 16 pontos em negrito. E, finalmente, um botão Fechar de 28 x 28 pixels posicionado a dois pixels da parte superior e a dois pixels da direita do contêiner da caixa de diálogo:

```
.s7ecatalogviewer .s7emaildialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgemail_cap.png"); 
    height: 17px; 
    width: 24px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogviewer .s7emaildialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7emaildialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

O rodapé da caixa de diálogo consiste nos botões Cancelar e Enviar email. O contêiner de rodapé é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogfooter
```

**Propriedades CSS do rodapé da caixa de diálogo &#x200B;**

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
.s7ecatalogviewer .s7emaildialog .s7dialogbuttoncontainer
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
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton
```

**Propriedades CSS do botão de cancelamento da caixa de diálogo**

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
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo do botão para cada estado. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão oferece suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

O botão Enviar email é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton
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
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo do botão para cada estado. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão oferece suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

Além disso, ambos os botões compartilham uma classe CSS comum, que pode conter configurações CSS que são as mesmas para outros botões da caixa de diálogo:

```
.s7ecatalogviewer .s7emaildialog .s7dialogfooter .s7button
```

**Propriedades CSS do botão**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> espessura da fonte </span> </p> </td> 
   <td colname="col2"> <p>Peso da fonte do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Família de fontes <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p>Família de fontes do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura da linha </span> </p> </td> 
   <td colname="col2"> <p> Altura do texto dentro do botão. Afeta o alinhamento vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sombra-caixa </span> </p> </td> 
   <td colname="col2"> <p>Sombra projetada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem direita </span> </p> </td> 
   <td colname="col2"> <p>Margem direita do botão. </p> </td> 
  </tr> 
 </tbody> 
</table>

As dicas de ferramenta deste botão podem ser localizadas. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - Para configurar um rodapé de caixa de diálogo com o botão Cancelar 64 x 34 e um botão Enviar email 82 x 34. A cor do texto e a cor do plano de fundo são diferentes para cada estado do botão:

```
.s7ecatalogviewer .s7emaildialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

A área de diálogo principal, entre o cabeçalho e o rodapé, contém conteúdo de diálogo rolável e painel de rolagem à direita. Em todos os casos, o componente gerencia a largura dessa área. Não é possível defini-la no CSS. A área de diálogo principal é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogviewarea
```

**Propriedades CSS da área de exibição da caixa de diálogo &#x200B;**

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p> A altura da área da caixa de diálogo principal. Ela deve ser especificada somente quando a caixa de diálogo funciona no modo desktop. Não é aplicável quando a caixa de diálogo é dimensionada para ocupar toda a janela do navegador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>A cor de fundo da área da caixa de diálogo principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem </span> </p> </td> 
   <td colname="col2"> <p>Margem externa. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>A área da caixa de diálogo principal oferece suporte ao seletor de atributos `state` opcional. Está definido como `sendsuccess` quando o formulário de email é enviado e a caixa de diálogo mostra uma mensagem de confirmação. Desde que a mensagem de confirmação seja pequena, esse seletor de atributos pode ser usado para reduzir a altura da caixa de diálogo quando essa mensagem de confirmação é exibida.

Exemplo - para configurar a área da caixa de diálogo principal para uma altura inicial de 300 pixels e uma altura de 100 pixels quando a mensagem de confirmação for exibida, tenha uma margem de dez pixels e use um plano de fundo branco:

```
.s7ecatalogviewer .s7emaildialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogviewarea[state='sendsuccess'] { 
 height:100px; 
}
```

Todo o conteúdo do formulário (como rótulos e campos de entrada) reside dentro de um container controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody
```

Se a altura desse contêiner parecer ser maior que a área da caixa de diálogo principal, a rolagem vertical será ativada automaticamente pelo componente.

**Propriedades CSS do corpo da caixa de diálogo &#x200B;**

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar o conteúdo do formulário para ter um preenchimento de dez pixels:

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody { 
    padding: 10px; 
}
```

O formulário da caixa de diálogo é preenchido linha por linha, onde cada linha carrega uma parte do conteúdo do formulário (como um rótulo e um campo de entrada de texto). A linha de formulário única é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody .s7dialogline
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

Exemplo - para configurar um formulário de caixa de diálogo com preenchimento de dez pixels para cada linha:

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

Todos os rótulos estáticos no formulário da caixa de diálogo são controlados com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialoglabel
```

Essa classe não é adequada para controlar o tamanho ou a posição dos rótulos, pois pode ser aplicada a textos em vários locais da interface do usuário do formulário.

**Propriedades CSS do rótulo da caixa de diálogo. &#x200B;**

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> espessura da fonte </span> </p> </td> 
   <td colname="col2"> <p>Espessura da fonte do rótulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte do rótulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Família de fontes <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p>Família de fontes do rótulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto do rótulo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Os rótulos da caixa de diálogo podem ser localizados. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - para configurar todos os rótulos para serem cinza, negrito, com uma fonte de nove pixels:

```
.s7ecatalogviewer .s7emaildialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

Todos os rótulos estáticos exibidos à esquerda dos campos de entrada de formulário são controlados com:

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputlabel
```

**Propriedades CSS do rótulo de entrada da caixa de diálogo**

<table id="table_B5CF02837BAA42C7B79B6D9DA20792DF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>A largura do rótulo estático. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>O alinhamento do texto horizontal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem </span> </p> </td> 
   <td colname="col2"> <p>Margem do rótulo estático. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento estático do rótulo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar rótulos de campo de entrada com largura de 50 pixels, alinhados à direita, têm dez pixels de preenchimento e uma margem de dez pixels à direita:

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputlabel { 
    margin-right: 10px; 
    padding: 10px; 
    text-align: right; 
    width: 50px; 
}
```

Cada campo de entrada de formulário é colocado no container que permite aplicar uma borda personalizada ao redor do campo de entrada. Ele é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputcontainer
```

**Propriedades CSS do contêiner de entrada da caixa de diálogo**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borda </span> </p> </td> 
   <td colname="col2"> <p>Borda ao redor do container do campo de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>O contêiner de campo de entrada dá suporte ao seletor de atributo `state` opcional. Está definido como `verifyerror` quando o usuário comete um erro no formato de dados de entrada e a validação em linha falha. Esse seletor de atributo pode ser usado para realçar entradas de usuário incorretas no formulário.

A maioria dos campos de entrada que se espalham do rótulo à esquerda até a borda direita do corpo da caixa de diálogo (que inclui o campo De e o campo Mensagem) são controlados com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputwide
```

**Propriedades CSS do campo de entrada da caixa de diálogo**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do campo de entrada. </p> </td> 
  </tr> 
 </tbody> 
</table>

O campo Para é mais estreito porque aloca espaço para o botão Remover email à direita. Ele é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputshort
```

**Propriedades CSS do campo curto de entrada da caixa de diálogo**

<table id="table_DFA9059209FF4184BD483A529424E97F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do campo de entrada. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - Para configurar um formulário para ter uma borda cinza de um pixel com nove pixels de preenchimento ao redor de todos os campos de entrada. Ter a mesma borda em vermelho para campos com falha na validação. Para ter 250 pixels de largura para o campo. E, por fim, o restante dos campos de entrada com 300 pixels de largura:

```
.s7ecatalogviewer .s7emaildialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialoginputcontainer[state="verifyerror"] { 
    border: 1px solid #FF0000; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialoginputshort { 
    width: 250px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialoginputwide { 
    width: 300px; 
}
```

O campo de entrada de mensagens de email também é controlado com:

```
.s7ecatalogviewer .s7emaildialog .s7dialogmessage
```

Essa classe permite que você defina propriedades específicas para o elemento `TEXTAREA` subjacente.

**Propriedades CSS da mensagem da caixa de diálogo**

<table id="table_9E9D5A0C3CDB45739615C4C07F8DC046"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura da mensagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> quebra automática de linha </span> </p> </td> 
   <td colname="col2"> <p>Estilo de quebra de linha. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma mensagem de email com 50 pixels de altura e usar a quebra automática de linha `break-word`:

```
.s7ecatalogviewer .s7emaildialog .s7dialogmessage { 
    height: 50px; 
    word-wrap: break-word; 
}
```

O botão Adicionar outro endereço de email permite que um usuário adicione mais de um endereço no formulário de email. Ele é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton
```

**Propriedades CSS do botão adicionar endereço de email da caixa de diálogo**

<table id="table_8829DC0694684E8BA427DFB821F7433D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto do botão para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p>Imagem do botão para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Posição da imagem do botão dentro da área do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> espessura da fonte </span> </p> </td> 
   <td colname="col2"> <p>Peso da fonte do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Família de fontes <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p>Família de fontes do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura da linha </span> </p> </td> 
   <td colname="col2"> <p>Altura do texto dentro do botão. Afeta o alinhamento vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Alinhamento de texto horizontal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão oferece suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - para configurar o botão &quot;Adicionar outro endereço de email&quot; com 25 pixels de altura, use a fonte em negrito de 12 pontos com alinhamento à direita e uma cor de texto e imagem diferentes para cada estado:

```
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton { 
 text-align:right; 
 font-size:12pt; 
 font-weight:bold; 
 background-position:left center; 
 line-height:25px; 
 padding-left:30px; 
 height:25px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton[state='up'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton[state='down'] { 
 color:#000000; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton[state='over'] { 
 color:#000000; 
 text-decoration:underline; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogaddemailbutton[state='disabled'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
}
```

O botão Remover permite que um usuário remova endereços extras do formulário de email. Ele é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton
```

**Propriedades CSS do botão Remover email da caixa de diálogo**

<table id="table_79E4C65741E64859B9C9E9DCCB3D050B"> 
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
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p>Imagem do botão para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão oferece suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - para configurar um botão Remover para ter 25 x 25 pixels e usar uma imagem diferente para cada estado:

```
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton { 
 width:25px; 
 height:25px; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton[state='up'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton[state='over'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton[state='down'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogremoveemailbutton[state='disabled'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
}
```

O conteúdo que está sendo compartilhado é exibido na parte inferior do corpo da caixa de diálogo e inclui uma miniatura, título, URL de origem e descrição. Ele é colocado em um contêiner controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody .s7dialogcontent
```

**Propriedades CSS do conteúdo da caixa de diálogo &#x200B;**

<table id="table_9C5CBFC2482E4A46BE837573B0B02FE4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borda </span> </p> </td> 
   <td colname="col2"> <p>Borda do container. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um contêiner inferior para ter uma borda pontilhada de um pixel e nenhum preenchimento:

```
.s7ecatalogviewer .s7emaildialog .s7dialogbody .s7dialogcontent { 
    border: 1px dotted #A0A0A0; 
    padding: 0; 
}
```

A imagem em miniatura é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogthumbnail
```

A propriedade `background-image` é definida pela lógica do componente.

**Propriedades CSS da imagem em miniatura da caixa de diálogo**

<table id="table_4C614FF2CEB149DAB5B7D7BC38CD3CAE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura da miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura da miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alinhamento vertical </span> </p> </td> 
   <td colname="col2"> <p>Miniatura de alinhamento vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar a miniatura como 90 x 60 pixels e alinhada à parte superior com dez pixels de preenchimento:

```
.s7ecatalogviewer .s7emaildialog .s7dialogthumbnail { 
    height: 60px; 
    padding: 10px; 
    vertical-align: top; 
    width: 90px; 
}
```

O título, a origem e a descrição do conteúdo são agrupados ainda mais em um painel à direita da miniatura do conteúdo. Ele é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialoginfopanel
```

**Propriedades CSS do painel de informações da caixa de diálogo**

<table id="table_EDFA6229D8C3468E989E7EC05F23EF3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do painel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um painel de informações de conteúdo com 300 pixels de largura:

```
.s7ecatalogviewer .s7emaildialog .s7dialoginfopanel { 
    width: 300px; 
}
```

O título do conteúdo é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogtitle
```

**Propriedades CSS do título da caixa de diálogo**

<table id="table_E83C149E66EC474092DF8A180DA9A550"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem </span> </p> </td> 
   <td colname="col2"> <p>Margem externa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> espessura da fonte </span> </p> </td> 
   <td colname="col2"> <p>Peso da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Família de fontes <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p>Família da fonte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um título de conteúdo para usar fonte em negrito e ter uma margem de dez pixels:

```
.s7ecatalogviewer .s7emaildialog .s7dialogtitle { 
    font-weight: bold; 
    margin: 10px; 
}
```

A origem do conteúdo é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogorigin
```

**Propriedades CSS da origem do conteúdo da caixa de diálogo &#x200B;**

<table id="table_51763B532A9C4AE8AE54B69933A8C0B5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem </span> </p> </td> 
   <td colname="col2"> <p>Margem externa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> espessura da fonte </span> </p> </td> 
   <td colname="col2"> <p>Peso da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Família de fontes <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p>Família da fonte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar a origem do conteúdo para ter uma margem de dez pixels:

```
.s7ecatalogviewer .s7emaildialog .s7dialogorigin { 
    margin: 10px; 
}
```

A descrição do conteúdo é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogdescription
```

**Propriedades CSS da descrição do conteúdo da caixa de diálogo**

<table id="table_F0F917ED3D1D4FCE974F48214D287E14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem </span> </p> </td> 
   <td colname="col2"> <p>Margem externa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> espessura da fonte </span> </p> </td> 
   <td colname="col2"> <p>Peso da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Família de fontes <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p>Família da fonte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma descrição de conteúdo com uma margem de dez pixels e usar uma fonte de nove pontos:

```
.s7ecatalogviewer .s7emaildialog .s7dialogdescription { 
    font-size: 9pt; 
    margin: 10px; 
}
```

Quando um usuário insere dados de entrada incorretos e a validação em linha falha. Ou, quando a caixa de diálogo precisar renderizar uma mensagem de erro ou de confirmação quando o formulário for enviado, uma mensagem será exibida na parte superior do corpo da caixa de diálogo. Ele é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogerrormessage
```

**Propriedades CSS da mensagem de erro da caixa de diálogo**

<table id="table_C114E1004C334D339C25A3438E8E6614"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p> Ícone de erro. O padrão é um ponto de exclamação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posição do ícone de erro dentro da área de mensagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto da mensagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> espessura da fonte </span> </p> </td> 
   <td colname="col2"> <p>Peso da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Família de fontes <span class="codeph"> </span> </p> </td> 
   <td colname="col2"> <p>Família da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura da linha </span> </p> </td> 
   <td colname="col2"> <p> Altura do texto dentro da mensagem. Afeta o alinhamento vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esta mensagem dá suporte ao seletor de atributos `state` com os seguintes valores possíveis: `verifyerror`, `senderror` e `sendsuccess`. O valor `verifyerror` é definido quando uma mensagem é exibida devido a uma falha de validação de entrada em linha. O valor `senderror` é definido quando um serviço de email de back-end relata um erro. O valor `sendsuccess` é definido quando o email é enviado com êxito. Dessa forma, é possível estilizar a mensagem de forma diferente, dependendo do estado da caixa de diálogo.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - Para configurar uma mensagem para usar uma fonte em negrito de dez pontos, tenha 25 pixels de altura de linha, 20 pixels de preenchimento à esquerda e use um ícone de ponto de exclamação. E, por fim, texto vermelho se houver um erro, e nenhum ícone e texto verde se houver sucesso:

```
.s7ecatalogviewer .s7emaildialog .s7dialogerrormessage[state="verifyerror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogerrormessage[state="senderror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogerrormessage[state="sendsuccess"] { 
    background-image: none; 
    color: #00B200; 
} 
.s7ecatalogviewer .s7emaildialog .s7dialogerrormessage { 
    background-position: left center; 
    font-size: 10pt; 
    font-weight: bold; 
    line-height: 25px; 
    padding-left: 20px; 
}
```

Se a rolagem vertical for necessária, a barra de rolagem será renderizada no painel próximo à borda direita da caixa de diálogo, que é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7dialogscrollpanel
```

**Propriedades CSS do painel de rolagem da caixa de diálogo**

<table id="table_A0C3AC7E00544FFBB8E1364F4CDDB371"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do painel de rolagem </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um painel de rolagem com 44 pixels de largura:

```
.s7ecatalogviewer .s7emaildialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

A aparência da área da barra de rolagem é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar
```

**Propriedades CSS da barra de rolagem**

<table id="table_2BF74CF43E9B42D79F99A3F5208D7051"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p> A largura da barra de rolagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> O deslocamento da barra de rolagem vertical na parte superior do painel de rolagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> </span> inferior </p> </td> 
   <td colname="col2"> <p> O deslocamento da barra de rolagem vertical na parte inferior do painel de rolagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> direita </span> </p> </td> 
   <td colname="col2"> <p> O deslocamento da barra de rolagem horizontal em relação à borda direita do painel de rolagem. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma barra de rolagem com 28 pixels de largura, uma margem de oito pixels na parte superior, direita e inferior do painel de rolagem:

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

A faixa da barra de rolagem é a área entre os botões de rolagem superior e inferior. O componente define automaticamente a posição e a altura da faixa. A faixa é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolltrack
```

**Propriedades CSS da faixa de rolagem**

<table id="table_EE990E7A342843619EDD84BAD29C6F2A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>A largura da faixa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>A cor do plano de fundo da faixa. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma faixa de barra de rolagem com 28 pixels de largura e um plano de fundo cinza:

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

A miniatura da barra de rolagem se move verticalmente em uma área de rastreamento de rolagem. Sua posição vertical é totalmente controlada pela lógica do componente, no entanto, a altura da miniatura não muda dinamicamente dependendo da quantidade de conteúdo. Você pode configurar a altura da miniatura e outros aspectos com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb
```

**Propriedades CSS da miniatura da barra de rolagem**

<table id="table_5A4A283A50044A51881D997885674BDF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>A largura da miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>A altura do polegar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top </span> </p> </td> 
   <td colname="col2"> <p> O preenchimento vertical entre o topo da faixa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento inferior </span> </p> </td> 
   <td colname="col2"> <p> O preenchimento vertical entre a parte inferior da faixa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p>A imagem exibida para um determinado estado de miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>A miniatura dá suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de miniatura diferentes: `up`, `down`, `over` e `disabled`.

Exemplo - para configurar a miniatura da barra de rolagem com 28 x 45 pixels, tem uma margem de dez pixels na parte superior e inferior e tem um trabalho artístico diferente para cada estado:

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

A aparência dos botões de rolagem superior e inferior é controlada com os seguintes seletores de classe CSS:

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton
```

Não é possível posicionar botões de rolagem usando propriedades CSS `top`, `left`, `bottom` e `right`. Em vez disso, a lógica do visualizador as posiciona automaticamente.

**Propriedades CSS dos botões de rolagem superior e inferior**

<table id="table_EB853317E08941979B0E141C3C9B2C49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>A largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>A altura do botão. </p> </td> 
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
>Estes botões oferecem suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes: `up`, `down`, `over` e `disabled`.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - para configurar botões de rolagem com 28 x 32 pixels e que tenham arte-final diferente para cada estado:

```
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7ecatalogviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```
