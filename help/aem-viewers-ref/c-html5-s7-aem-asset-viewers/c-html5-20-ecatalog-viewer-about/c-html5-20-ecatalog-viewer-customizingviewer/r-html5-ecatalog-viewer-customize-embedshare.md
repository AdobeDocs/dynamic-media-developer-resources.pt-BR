---
description: A ferramenta de compartilhamento integrado consiste em um botão adicionado ao painel Compartilhamento social e a caixa de diálogo modal que é exibida quando a ferramenta é ativada. A posição do botão é totalmente gerenciada pela ferramenta de compartilhamento Social .
solution: Experience Manager
title: Compartilhamento incorporado
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '2610'
ht-degree: 0%

---


# Incorporar compartilhamento{#embed-share}

A ferramenta de compartilhamento integrado consiste em um botão adicionado ao painel Compartilhamento social e a caixa de diálogo modal que é exibida quando a ferramenta é ativada. A posição do botão é totalmente gerenciada pela ferramenta de compartilhamento Social .

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A aparência do botão de compartilhamento incorporado é controlada pelo seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embedshare
```

**Propriedades CSS da ferramenta de compartilhamento incorporada**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p> A imagem exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esse botão suporta o seletor de atributos `state`, que pode ser usado para aplicar skins diferentes a estados de botão diferentes.

É possível remover o botão do painel Compartilhamento do Social definindo `display:none` propriedade CSS em sua classe CSS.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - para configurar um botão de compartilhamento incorporado com 28 x 28 pixels e exibe uma imagem diferente para cada um dos quatro estados de botão diferentes:

```
.s7ecatalogviewer .s7embedshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7embedshare[state='up'] { 
background-image:url(images/v2/EmbedShare_dark_up.png); 
} 
.s7ecatalogviewer .s7embedshare[state='over'] { 
background-image:url(images/v2/EmbedShare_dark_over.png); 
} 
.s7ecatalogviewer .s7embedshare[state='down'] { 
background-image:url(images/v2/EmbedShare_dark_down.png); 
} 
.s7ecatalogviewer .s7embedshare[state='disabled'] { 
background-image:url(images/v2/EmbedShare_dark_disabled.png); 
}
```

A sobreposição em segundo plano que abrange a página da Web quando a caixa de diálogo está ativa é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7backoverlay
```

**Propriedades CSS da sobreposição em segundo plano**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidade  </span> </p> </td> 
   <td colname="col2"> <p>Opacidade da sobreposição em segundo plano. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor da sobreposição do plano de fundo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma sobreposição de plano de fundo para ficar cinza com 70% de opacidade:

```
.s7ecatalogviewer .s7embeddialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Por padrão, a caixa de diálogo modal é exibida centralizada na tela em sistemas de desktop e leva toda a área da página da Web em dispositivos de toque. Em todos os casos, o posicionamento e o dimensionamento da caixa de diálogo são gerenciados pelo componente . A caixa de diálogo é controlada com o seguinte seletor de classe CSS:

```
.s7embeddialog .s7dialog
```

**Propriedades CSS da caixa de diálogo**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> Raio da borda da caixa de diálogo, caso a caixa de diálogo não use o navegador inteiro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor de fundo da caixa de diálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Deve ser desativado ou definido como 100%, nesse caso, a caixa de diálogo ocupa toda a janela do navegador (esse modo é preferencial em dispositivos de toque). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Deve ser desativado ou definido como 100%, nesse caso, a caixa de diálogo ocupa toda a janela do navegador (esse modo é preferencial em dispositivos de toque). </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar a caixa de diálogo para usar toda a janela do navegador e ter um plano de fundo branco em dispositivos de toque:

```
.s7ecatalogviewer .s7touchinput .s7embeddialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

O cabeçalho da caixa de diálogo consiste em um ícone, um texto de título e um botão fechar. O contêiner de cabeçalho é controlado com

```
.s7ecatalogviewer .s7embeddialog .s7dialogheader
```

**Propriedades CSS do cabeçalho da caixa de diálogo**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento  </span> </p> </td> 
   <td colname="col2"> <p> Preenchimento interno para o conteúdo do cabeçalho. </p> </td> 
  </tr> 
 </tbody> 
</table>

O ícone e o texto do título são envolvidos em um contêiner adicional controlado com

```
.s7ecatalogviewer .s7embeddialog .s7dialogheader .s7dialogline
```

**Propriedades CSS da linha de diálogo**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento  </span> </p> </td> 
   <td colname="col2"> <p> Preenchimento interno para o ícone e o título do cabeçalho </p> </td> 
  </tr> 
 </tbody> 
</table>

O ícone Cabeçalho é controlado com o seguinte seletor de classe CSS

```
.s7ecatalogviewer .s7embeddialog .s7dialogheadericon
```

**Propriedades CSS do ícone de cabeçalho da caixa de diálogo**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura do ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Imagem do ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

O título do cabeçalho é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogheadertext
```

**Propriedades CSS do texto do cabeçalho da caixa de diálogo**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>Espessura da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte  </span> </p> </td> 
   <td colname="col2"> <p>Altura da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Família de fontes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento  </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento de texto interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

O botão Fechar é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7closebutton
```

**Propriedades CSS do botão Fechar **

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> Posição do botão vertical em relação ao contêiner de cabeçalho. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p> Posição do botão horizontal em relação ao contêiner de cabeçalho. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento  </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Imagem do botão para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esse botão suporta o seletor de atributos `state`, que pode ser usado para aplicar skins diferentes a estados de botão diferentes.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - para configurar o cabeçalho da caixa de diálogo com o preenchimento, o ícone de 24 x 14 pixels, o título de 16 pontos em negrito e o botão de fechamento de 28 x 28 pixels, posicionados dois pixels da parte superior e dois pixels da direita do contêiner da caixa de diálogo:

```
.s7ecatalogviewer .s7embeddialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgembed_cap.png"); 
    height: 14px; 
    width: 24px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogviewer .s7embeddialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7embeddialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

O rodapé da caixa de diálogo consiste no botão &quot;cancelar&quot;. O contêiner de rodapé é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogfooter
```

**Propriedades CSS do rodapé da caixa de diálogo **

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p> Borda que você pode usar para separar visualmente o rodapé do restante da caixa de diálogo. </p> </td> 
  </tr> 
 </tbody> 
</table>

O rodapé tem um contêiner interno que mantém o botão. É controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogbuttoncontainer
```

**Propriedades CSS do contêiner do botão da caixa de diálogo**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento  </span> </p> </td> 
   <td colname="col2"> <p> Preenchimento interno entre o rodapé e o botão. </p> </td> 
  </tr> 
 </tbody> 
</table>

O botão Selecionar tudo é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton
```

O botão só está disponível em sistemas de desktop.

**Propriedades CSS do botão Selecionar tudo**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p> Cor do texto do botão para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p> Cor de fundo do botão para cada estado. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>O botão Selecionar tudo suporta o seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

O botão Cancelar é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton
```

**Propriedades CSS do botão Cancelar da caixa de diálogo**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p> Cor do texto do botão para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p> Cor de fundo do botão para cada estado. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esse botão suporta o seletor de atributos `state`, que pode ser usado para aplicar skins diferentes a estados de botão diferentes.

Além disso, ambos os botões compartilham a mesma classe CSS comum que pode conter configurações CSS que são as mesmas para outros botões de caixa de diálogo:

```
.s7ecatalogviewer .s7embeddialog .s7dialogfooter .s7button
```

**Propriedades CSS do botão**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>Espessura da fonte do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte  </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Família de fontes do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura da linha  </span> </p> </td> 
   <td colname="col2"> <p> Altura do texto dentro do botão. Afeta o alinhamento vertical. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sombra de caixa  </span> </p> </td> 
   <td colname="col2"> <p>Sombra. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem direita  </span> </p> </td> 
   <td colname="col2"> <p>Margem do botão direito. </p> </td> 
  </tr> 
 </tbody> 
</table>

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - para configurar um rodapé de caixa de diálogo com um botão Cancelar 64 x 34, um botão Selecionar tudo 82 x 34 e uma cor de texto e uma cor de plano de fundo diferentes para cada estado de botão:

```
.s7ecatalogviewer .s7embeddialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogviewer .s7embeddialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

A área de diálogo principal (entre o cabeçalho e o rodapé) contém conteúdo da caixa de diálogo rolável e o painel de rolagem à direita. Em todos os casos, o componente gerencia a largura dessa área, não é possível defini-la em CSS. A área de diálogo principal é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogviewarea
```

**Propriedades CSS da área de visualização da caixa de diálogo **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p> A altura da área da caixa de diálogo principal. Ela deve ser especificada somente quando a caixa de diálogo funcionar no modo de desktop. Não é aplicável quando a caixa de diálogo é dimensionada para ocupar toda a janela do navegador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>A cor de fundo da área da caixa de diálogo principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem  </span> </p> </td> 
   <td colname="col2"> <p>Margem externa. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma área da caixa de diálogo principal para ter 300 pixels de altura, tenha uma margem de dez pixels e use um plano de fundo branco:

```
.s7ecatalogviewer .s7embeddialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

Todo o conteúdo do formulário (como rótulos e campos de entrada) reside dentro de um contêiner controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogbody
```

Se a altura desse contêiner parecer ser maior que a área da caixa de diálogo principal, uma rolagem vertical é ativada automaticamente pelo componente.

**Propriedades CSS do corpo da caixa de diálogo **

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento  </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar o conteúdo do formulário para ter o preenchimento de dez pixels:

```
.s7ecatalogviewer .s7embeddialog .s7dialogbody { 
    padding: 10px; 
}
```

Todos os rótulos estáticos no formulário da caixa de diálogo são controlados com

```
.s7ecatalogviewer .s7embeddialog .s7dialoglabel
```

Essa classe não é adequada para controlar o tamanho ou a posição do rótulo, pois você pode aplicá-lo a textos em vários lugares da interface do usuário do formulário.

**Propriedades CSS do rótulo da caixa de diálogo. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>Espessura da fonte do rótulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> tamanho da fonte  </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte do rótulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Rotular família de fontes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto do rótulo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Os rótulos da caixa de diálogo podem ser localizados. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - para configurar todos os rótulos para serem cinza, negrito com uma fonte de nove pixels:

```
.s7ecatalogviewer .s7embeddialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

O tamanho da cópia de texto exibida na parte superior do código incorporado é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialoginputwide
```

**Propriedades CSS do campo de entrada da caixa de diálogo**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura do campo de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento  </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir a cópia de texto como 430 pixels de largura e ter um preenchimento de dez pixels na parte inferior:

```
.s7ecatalogviewer .s7embeddialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

O código incorporado é encapsulado em um contêiner e controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialoginputcontainer
```

**Propriedades CSS do contêiner de entrada da caixa de diálogo**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>A largura do contêiner de código incorporado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Borda em torno do contêiner de código incorporado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento  </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir uma borda cinza de um pixel em torno do texto do código incorporado, torne-a de 430 pixels de largura e tenha um preenchimento de dez pixels:

```
.s7ecatalogviewer .s7embeddialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 10px; 
    width: 430px; 
}
```

O texto real do código incorporado é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialoginputcontainer
```

**Propriedades CSS do contêiner de entrada da caixa de diálogo**

<table id="table_FEEF66150C69489BB42A2408EBFCE928"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> quebra automática  </span> </p> </td> 
   <td colname="col2"> <p>Estilo de quebra automática de palavra. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar o código incorporado para usar `break-word` quebra automática de palavra:

```
.s7ecatalogviewer .s7embeddialog .s7dialogmessage { 
    word-wrap: break-word; 
}
```

Incorporar rótulo de tamanho e lista suspensa estão localizados na parte inferior da caixa de diálogo e colocados em um contêiner controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogembedsizepanel
```

**Propriedades CSS do painel de tamanho da incorporação da caixa de diálogo**

<table id="table_6BA2769361BA4EC4AB7D250EC9486CB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento  </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um painel de tamanho incorporado para ter dez pixels de preenchimento:

```
.s7ecatalogviewer .s7embeddialog .s7dialogembedsizepanel { 
    padding: 10px; 
}
```

O tamanho e o alinhamento do rótulo de tamanho incorporado são controlados com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogembedsizepanel
```

**Propriedades CSS do painel de tamanho da incorporação da caixa de diálogo**

<table id="table_8E50C63C9B1349999251CDB5E5AD3D1D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alinhamento vertical  </span> </p> </td> 
   <td colname="col2"> <p>Alinhamento vertical do rótulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura do rótulo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir o rótulo de tamanho incorporado para ser alinhado no topo e 80 pixels de largura:

```
.s7ecatalogviewer .s7embeddialog .s7dialogembedsizelabel { 
    vertical-align: top; 
    width: 80px; 
}
```

A largura da caixa de combinação de tamanho incorporado é controlada pelo seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7combobox
```

**Propriedades CSS da caixa de combinação**

<table id="table_C0FEA0C7353F40039204641BB3F1AE14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura da caixa de combinação. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>A caixa combo suporta o seletor de atributos `expanded` com possíveis valores de `true` e `false`. `true` é usada quando a caixa de combinação exibe um dos tamanhos incorporados predefinidos, portanto, deve ter toda a largura disponível. `false` é usada quando a opção de tamanho personalizado está selecionada na caixa de combinação; portanto, deve ser reduzida para permitir espaço para campos de entrada de largura e altura personalizados.

Exemplo - para definir a caixa de combinação de tamanho incorporado com largura de 300 pixels ao mostrar um item predefinido e 110 pixels de largura ao mostrar um tamanho personalizado:

```
.s7ecatalogviewer .s7embeddialog .s7combobox[expanded="true"] { 
    width: 300px; 
} 
.s7ecatalogviewer .s7embeddialog .s7combobox[expanded="false"] { 
    width: 110px; 
}
```

A altura do texto da caixa de combinação é definida por um elemento interno especial e é controlada pelo seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxtext
```

**Propriedades CSS do texto da caixa de combinação**

<table id="table_AB60032BF337433F8455DE20AFBA29AB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do texto da caixa de combinação. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir a altura do texto da caixa de combinação do tamanho de incorporação como 40 pixels:

```
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxtext { 
    height: 40px; 
}
```

A caixa de combinação tem um botão &quot;suspenso&quot; à direita e é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton
```

**Propriedades CSS do botão da caixa de combinação**

<table id="table_70E127FA21264366AD5DBBD7DF40EBAA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Posição vertical do botão dentro da caixa de combinação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p>Posição do botão horizontal dentro da caixa de combinação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Imagem do botão para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esse botão suporta o seletor de atributos `state`, que pode ser usado para aplicar skins diferentes a estados de botão diferentes.

Exemplo - para definir um botão suspenso como 28 x 28 pixels e ter uma imagem separada para cada estado:

```
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='up'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='over'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='down'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='disabled'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
}
```

O painel com a lista de tamanhos incorporados exibidos quando a caixa de combinação é aberta é controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7comboboxdropdown
```

O tamanho e a posição do painel são controlados pelo componente. Não é possível alterá-lo por meio de CSS.

**Propriedades CSS da caixa de combinação suspensa**

<table id="table_FA7345321C6A4E63B4B78ECF81CE18DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Borda do painel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir o painel da caixa de combinação para ter uma borda cinza de um pixel:

```
.s7ecatalogviewer .s7embeddialog .s7comboboxdropdown { 
    border: 1px solid #CCCCCC; 
}
```

Um único item em um painel suspenso controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dropdownitemanchor
```

**Propriedades CSS da âncora suspensa do item**

<table id="table_FD42FDD56F89463A97FD292FAA04DA5A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p>Plano de fundo do item. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir o item de painel da caixa de combinação para ter um plano de fundo branco:

```
.s7ecatalogviewer .s7embeddialog .s7dropdownitemanchor { 
    background-color: #FFFFFF; 
}
```

Uma marca de seleção exibida à esquerda do item selecionado dentro do painel da caixa de combinação que é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7checkmark
```

**Propriedades CSS da caixa de seleção**

<table id="table_8E01F5461CD04AC18B2C3725A961476A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura do ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Imagem do item. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir o ícone de marca de seleção como 25 x 25 pixels:

```
.s7ecatalogviewer .s7embeddialog .s7checkmark { 
    background-image: url("images/sdk/cboxchecked.png"); 
    height: 25px; 
    width: 25px; 
}
```

Quando a opção &quot;Tamanho personalizado&quot; é selecionada na caixa de combinação de tamanho incorporado, a caixa de diálogo exibe dois campos de entrada extras à direita para permitir que o usuário insira um tamanho de incorporação personalizado. Esses campos são vinculados em um contêiner controlado pelo seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogcustomsizepanel
```

**Propriedades CSS do painel de tamanho personalizado da caixa de diálogo**

<table id="table_B00829EA550F4E5E8F51B1C6ADACCD34"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left  </span> </p> </td> 
   <td colname="col2"> <p> Distância da caixa de combinação de tamanho incorporado. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir o painel de campos de entrada de tamanho personalizado como 20 pixels à direita da caixa de combinação:

```
.s7ecatalogviewer .s7embeddialog .s7dialogcustomsizepanel { 
    left: 20px; 
}
```

Cada campo de entrada de tamanho personalizado é colocado em um contêiner que renderiza uma borda e define a margem entre os campos. É controlado com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogcustomsize
```

**Propriedades CSS do tamanho personalizado da caixa de diálogo**

<table id="table_A8A04BE1988641618D0A412B8AEEE1C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Borda em torno do campo de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p> Largura do campo de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem  </span> </p> </td> 
   <td colname="col2"> <p> Margem do campo de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento  </span> </p> </td> 
   <td colname="col2"> <p> Preenchimento do campo de entrada. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir os campos de entrada de tamanho personalizado para ter uma borda cinza, margem, preenchimento de um pixel e ter 70 pixels de largura:

```
.s7ecatalogviewer .s7embeddialog .s7dialogcustomsize { 
    border: 1px solid #CCCCCC; 
    margin-right: 20px; 
    padding-left: 2px; 
    padding-right: 2px; 
    width: 70px; 
}
```

Se a rolagem vertical for necessária, a barra de rolagem será renderizada no painel próximo à borda direita da caixa de diálogo, que é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7dialogscrollpanel
```

**Propriedades CSS do painel de rolagem da caixa de diálogo**

<table id="table_BA37E577E0884C919383F84080E2DD28"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura do painel de rolagem. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um painel de rolagem com largura de 44 pixels

```
.s7ecatalogviewer .s7embeddialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

A aparência da área da barra de rolagem é controlada com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar
```

**Propriedades de CSS da barra de rolagem**

<table id="table_066492417FCA43929017993D7326CDB8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura da barra de rolagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> O deslocamento vertical da barra de rolagem na parte superior do painel de rolagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p> O deslocamento vertical da barra de rolagem na parte inferior do painel de rolagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p> O deslocamento da barra de rolagem horizontal a partir da borda direita do painel de rolagem. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma barra de rolagem com 28 pixels de largura e uma margem de oito pixels da parte superior, direita e inferior do painel de rolagem:

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

O rastreamento da barra de rolagem é a área entre os botões de rolagem superior e inferior. O componente define automaticamente a posição e a altura da faixa. A faixa é controlada com o seguinte seletor de classe CSS

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolltrack
```

**Propriedades CSS do rastreamento da barra de rolagem**

<table id="table_19CF5503C1D34ED9998D4F4A6DA7D5D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura da faixa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor do fundo  </span> </p> </td> 
   <td colname="col2"> <p> Rastrear a cor do plano de fundo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um rastreamento de barra de rolagem com 28 pixels de largura e um plano de fundo cinza:

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

O polegar da barra de rolagem se move verticalmente em uma área de trilha de rolagem. Sua posição vertical é totalmente controlada pela lógica do componente. No entanto, a altura do polegar não muda dinamicamente, dependendo da quantidade de conteúdo. A altura do polegar e outros aspectos podem ser configurados com o seguinte seletor de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb
```

**Propriedades de CSS da barra de rolagem**

<table id="table_90BC468FE138441C9DBAB1EB109F3DB0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura do polegar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do polegar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte superior do preenchimento  </span> </p> </td> 
   <td colname="col2"> <p>O preenchimento vertical entre a parte superior da faixa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parte inferior do preenchimento  </span> </p> </td> 
   <td colname="col2"> <p> O preenchimento vertical entre a parte inferior da faixa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p> A imagem exibida para um determinado estado de polegar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>A miniatura suporta o seletor de atributos `state`, que pode ser usado para aplicar diferentes capas a diferentes estados de miniatura: `up`, `down`, `over` e `disabled`.

Exemplo - para configurar um polegar da barra de rolagem que seja 28 x 45 pixels, tenha uma margem de dez pixels na parte superior e inferior e tenha uma arte-final diferente para cada estado:

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

A aparência dos botões de rolagem superior e inferior é controlada pelos seguintes seletores de classe CSS:

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton
```

Não é possível posicionar botões de rolagem usando as propriedades CSS `top`, `left`, `bottom` e `right`. Em vez disso, a lógica do visualizador os posiciona automaticamente.

**Propriedades CSS dos botões de rolagem superior e inferior**

<table id="table_554BFCFEAF4F43A9AE5F741DC126F833"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Altura do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo  </span> </p> </td> 
   <td colname="col2"> <p> A imagem exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da estrutura de arte, se os sprites CSS forem usados. </p> <p>Consulte também <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Esses botões suportam o seletor de atributos `state`, que pode ser usado para aplicar skins diferentes a estados de botões diferentes: `up`, `down`, `over` e `disabled`.

As dicas de ferramentas do botão podem ser localizadas. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) para obter mais informações.

Exemplo - para configurar botões de rolagem que são 28 x 32 pixels e têm arte-final diferente para cada estado:

```
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7ecatalogviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```

