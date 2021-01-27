---
description: A ferramenta de compartilhamento de links consiste em um botão adicionado ao painel Compartilhamento em redes sociais e a caixa de diálogo modal que é exibida quando a ferramenta é ativada. A posição do botão é totalmente gerenciada pela ferramenta de compartilhamento do Social.
seo-description: A ferramenta de compartilhamento de links consiste em um botão adicionado ao painel Compartilhamento em redes sociais e a caixa de diálogo modal que é exibida quando a ferramenta é ativada. A posição do botão é totalmente gerenciada pela ferramenta de compartilhamento do Social.
seo-title: Compartilhamento de links
solution: Experience Manager
title: Compartilhamento de links
topic: Dynamic Media
uuid: 699ddab2-8cfd-4edf-bb1b-5ff91fe63c1a
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '1415'
ht-degree: 0%

---


# Compartilhamento de link{#link-share}

A ferramenta de compartilhamento de links consiste em um botão adicionado ao painel Compartilhamento em redes sociais e a caixa de diálogo modal que é exibida quando a ferramenta é ativada. A posição do botão é totalmente gerenciada pela ferramenta de compartilhamento do Social.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

A aparência do botão de compartilhamento de link é controlada com o seguinte seletor de classe CSS:

```
.s7videoviewer .s7linkshare
```

**Propriedades de CSS da ferramenta de compartilhamento de links**

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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> A imagem que é exibida para um determinado estado de botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da sprite de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão suporta o seletor de atributos `state`, que pode ser usado para aplicar diferentes capas a diferentes estados de botão.

É possível remover o botão do painel Compartilhamento em redes sociais definindo `display:none` a propriedade CSS em sua classe CSS.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização de elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obter mais informações.

Exemplo - para configurar um botão de compartilhamento de link com 28 x 28 pixels e exibe uma imagem diferente para cada um dos quatro estados de botão diferentes:

```
.s7videoviewer .s7linkshare { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7linkshare[state='up'] { 
background-image:url(images/v2/LinkShare_dark_up.png); 
} 
.s7videoviewer .s7linkshare[state='over'] { 
background-image:url(images/v2/LinkShare_dark_over.png); 
} 
.s7videoviewer .s7linkshare[state='down'] { 
background-image:url(images/v2/LinkShare_dark_down.png); 
} 
.s7videoviewer .s7linkshare[state='disabled'] { 
background-image:url(images/v2/LinkShare_dark_disabled.png); 
}
```

A sobreposição em segundo plano que abrange a página da Web quando a caixa de diálogo está ativa é controlada pelo seguinte seletor de classe CSS:

```
.s7videoviewer .s7linkdialog .s7backoverlay
```

**Propriedades de CSS da sobreposição de plano de fundo**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidade  </span> </p> </td> 
   <td colname="col2"> <p>Opacidade da sobreposição em segundo plano. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor da sobreposição do plano de fundo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma sobreposição de plano de fundo para ficar cinza com 70% de opacidade:

```
.s7videoviewer .s7linkdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Por padrão, a caixa de diálogo modal é exibida centralizada na tela nos sistemas de desktop e leva toda a área da página da Web para os dispositivos de toque. Em todos os casos, o posicionamento e o dimensionamento da caixa de diálogo são gerenciados pelo componente. A caixa de diálogo é controlada com o seguinte seletor de classe CSS:

```
.s7videoviewer .s7linkdialog .s7dialog
```

**Propriedades de CSS da caixa de diálogo**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> raio da borda  </span> </p> </td> 
   <td colname="col2"> <p> Raio da borda da caixa de diálogo, caso a caixa de diálogo não use o navegador inteiro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p>Cor de fundo da caixa de diálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Deve ser desdefinido ou definido como 100%, caso em que a caixa de diálogo pega a janela inteira do navegador (este modo é preferencial em dispositivos de toque). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p>Deve ser desdefinido ou definido como 100%, caso em que a caixa de diálogo pega a janela inteira do navegador (este modo é preferencial em dispositivos de toque). </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar a caixa de diálogo para usar toda a janela do navegador e ter um plano de fundo branco em dispositivos de toque:

```
.s7videoviewer .s7touchinput .s7linkdialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

O cabeçalho da caixa de diálogo consiste em um ícone, um texto de título e um botão de fechamento. O container header é controlado com

```
.s7videoviewer .s7linkdialog .s7dialogheader
```

**Propriedades de CSS do cabeçalho da caixa de diálogo**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> revestimento  </span> </p> </td> 
   <td colname="col2"> <p> Preenchimento interno para o conteúdo do cabeçalho. </p> </td> 
  </tr> 
 </tbody> 
</table>

O ícone e o texto do título são vinculados em um container adicional controlado com

```
.s7videoviewer .s7linkdialog .s7dialogheader .s7dialogline
```

**Propriedades de CSS da linha de diálogo**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> revestimento  </span> </p> </td> 
   <td colname="col2"> <p> Preenchimento interno para o ícone e o título do cabeçalho </p> </td> 
  </tr> 
 </tbody> 
</table>

O ícone de cabeçalho é controlado com o seguinte seletor de classe CSS

```
.s7videoviewer .s7linkdialog .s7dialogheadericon
```

**Propriedades de CSS do ícone de cabeçalho da caixa de diálogo**

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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Imagem do ícone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da sprite de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

O título do cabeçalho é controlado com o seguinte seletor de classe CSS:

```
.s7videoviewer .s7linkdialog .s7dialogheadertext
```

**Propriedades de CSS do texto do cabeçalho da caixa de diálogo**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-peso  </span> </p> </td> 
   <td colname="col2"> <p>Peso de fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Altura da fonte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Família de fontes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> revestimento  </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento de texto interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

O botão Fechar é controlado com o seguinte seletor de classe CSS:

```
.s7videoviewer .s7linkdialog .s7closebutton
```

**Propriedades CSS do botão Fechar **

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> Posição vertical do botão em relação ao container do cabeçalho. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p> Posição do botão horizontal em relação ao container do cabeçalho. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> revestimento  </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Imagem do botão para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posição de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Posição dentro da sprite de arte, se os sprites CSS forem usados. </p> <p>Consulte <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão suporta o seletor de atributos `state`, que pode ser usado para aplicar diferentes capas a diferentes estados de botão.

A dica de ferramenta do botão Fechar e o título da caixa de diálogo podem ser localizados. Consulte [Localização de elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obter mais informações.

Exemplo - para configurar um cabeçalho de caixa de diálogo com preenchimento, ícone de 22 x 12 pixels, título de 16 pontos em negrito e um botão Fechar de 28 x 28 pixels posicionado dois pixels da parte superior e dois pixels à direita do container da caixa de diálogo:

```
.s7videoviewer .s7linkdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7videoviewer .s7linkdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7videoviewer .s7linkdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlglink_cap.png"); 
    height: 12px; 
    width: 22px; 
} 
.s7videoviewer .s7linkdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7videoviewer .s7linkdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7linkdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7videoviewer .s7linkdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7videoviewer .s7linkdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7videoviewer .s7linkdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

O rodapé da caixa de diálogo consiste no botão &quot;cancelar&quot;. O container de rodapé é controlado com o seguinte seletor de classe CSS:

```
.s7videoviewer .s7linkdialog .s7dialogfooter
```

**Propriedades CSS do rodapé da caixa de diálogo **

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fronteira  </span> </p> </td> 
   <td colname="col2"> <p> Borda que você pode usar para separar visualmente o rodapé do restante da caixa de diálogo. </p> </td> 
  </tr> 
 </tbody> 
</table>

O rodapé tem um container interno que mantém o botão. É controlado com o seguinte seletor de classe CSS:

```
.s7videoviewer .s7linkdialog .s7dialogbuttoncontainer
```

**Propriedades de CSS do container do botão da caixa de diálogo**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> revestimento  </span> </p> </td> 
   <td colname="col2"> <p> Preenchimento interno entre o rodapé e o botão. </p> </td> 
  </tr> 
 </tbody> 
</table>

O botão Selecionar tudo é controlado com o seguinte seletor de classe CSS:

```
.s7videoviewer .s7linkdialog .s7dialogactionbutton
```

O botão só está disponível em sistemas de desktop.

**Propriedades de CSS do botão Selecionar tudo**

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
   <td colname="col1"> <p> <span class="codeph"> cor  </span> </p> </td> 
   <td colname="col2"> <p> Cor do texto do botão para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Cor de fundo do botão para cada estado. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>O botão Selecionar tudo suporta o seletor de atributos `state`, que pode ser usado para aplicar diferentes capas a diferentes estados de botão.

O botão Cancelar é controlado com o seguinte seletor de classe CSS:

```
.s7videoviewer .s7linkdialog .s7dialogcancelbutton
```

**Propriedades de CSS do botão Cancelar da caixa de diálogo**

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
   <td colname="col1"> <p> <span class="codeph"> cor  </span> </p> </td> 
   <td colname="col2"> <p> Cor do texto do botão para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p> Cor de fundo do botão para cada estado. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão suporta o seletor de atributos `state`, que pode ser usado para aplicar diferentes capas a diferentes estados de botão.

Além disso, ambos os botões compartilham a mesma classe CSS comum que pode conter configurações CSS que são as mesmas para outros botões da caixa de diálogo:

```
.s7videoviewer .s7linkdialog .s7dialogfooter .s7button
```

**Propriedades de CSS do botão**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-peso  </span> </p> </td> 
   <td colname="col2"> <p>Peso de fonte do botão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
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

As dicas de ferramentas do botão podem ser localizadas. Consulte [Localização de elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obter mais informações.

Exemplo - para configurar um rodapé de caixa de diálogo com um botão Cancelar 64 x 34, com a cor do texto e a cor do plano de fundo diferentes para cada estado do botão:

```
.s7videoviewer .s7linkdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7videoviewer .s7linkdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7videoviewer .s7linkdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7videoviewer .s7linkdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7videoviewer .s7linkdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7videoviewer .s7linkdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7linkdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7linkdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7videoviewer .s7linkdialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7videoviewer .s7linkdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7videoviewer .s7linkdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7linkdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7linkdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

A área de diálogo principal (entre o cabeçalho e o rodapé) contém conteúdo da caixa de diálogo. Em todos os casos, o componente gerencia a largura dessa área — não é possível defini-la em CSS. A área de diálogo principal é controlada com o seguinte seletor de classe CSS:

```
.s7videoviewer .s7linkdialog .s7dialogviewarea
```

**Propriedades CSS da área de visualização da caixa de diálogo **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura  </span> </p> </td> 
   <td colname="col2"> <p> A altura da área da caixa de diálogo principal. Ela deve ser especificada somente quando a caixa de diálogo funciona no modo de área de trabalho. Não é aplicável quando a caixa de diálogo é dimensionada para ocupar a janela inteira do navegador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo  </span> </p> </td> 
   <td colname="col2"> <p>A cor de plano de fundo da área da caixa de diálogo principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem  </span> </p> </td> 
   <td colname="col2"> <p>Margem externa. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma área da caixa de diálogo principal para ter 300 pixels de altura, ter uma margem de dez pixels e usar um plano de fundo branco:

```
.s7videoviewer .s7linkdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

Todo o conteúdo do formulário (como rótulos e campos de entrada) reside em um container controlado com

```
.s7videoviewer .s7linkdialog .s7dialogbody
```

**Propriedades CSS do corpo da caixa de diálogo **

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> revestimento  </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar o conteúdo do formulário para ter dez pixels de preenchimento:

```
.s7videoviewer .s7linkdialog .s7dialogbody { 
    padding: 10px; 
}
```

Todos os rótulos estáticos no formulário da caixa de diálogo são controlados com

```
.s7videoviewer .s7linkdialog .s7dialoglabel
```

Essa classe não é adequada para controlar o tamanho ou a posição da etiqueta, pois é possível aplicá-la a textos em vários locais da interface do usuário do formulário.

**Propriedades CSS do rótulo da caixa de diálogo. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-peso  </span> </p> </td> 
   <td colname="col2"> <p>Peso de fonte do rótulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Tamanho da fonte do rótulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> família de fontes  </span> </p> </td> 
   <td colname="col2"> <p>Família de fontes de etiquetas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor  </span> </p> </td> 
   <td colname="col2"> <p>Cor do texto do rótulo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Os rótulos da caixa de diálogo podem ser localizados. Consulte [Localização de elementos da interface do usuário](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obter mais informações.

Exemplo - para configurar todos os rótulos como cinza, negrito com uma fonte de nove pixels:

```
.s7videoviewer .s7linkdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

O tamanho da cópia de texto exibida na parte superior do link é controlado com o seguinte seletor de classe CSS:

```
.s7videoviewer .s7linkdialog .s7dialoginputwide
```

**Propriedades de CSS do campo de entrada da caixa de diálogo**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Largura do texto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> revestimento  </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir a cópia de texto com largura de 430 pixels e ter um preenchimento de dez pixels na parte inferior:

```
.s7videoviewer .s7linkdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

O link de compartilhamento é encapsulado em um container e controlado com o seguinte seletor de classe CSS:

```
.s7videoviewer .s7linkdialog .s7dialoginputcontainer
```

**Propriedades de CSS do container de entrada da caixa de diálogo**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fronteira  </span> </p> </td> 
   <td colname="col2"> <p>Borda em torno do container de link de compartilhamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> revestimento  </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir uma borda cinza de um pixel ao redor do texto do código incorporado e ter nove pixels de preenchimento:

```
.s7videoviewer .s7linkdialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
}
```

O próprio link de compartilhamento é controlado com o seguinte seletor de classe CSS:

```
.s7videoviewer .s7linkdialog .s7dialoglink
```

**Propriedades de CSS do link de compartilhamento da caixa de diálogo**

<table id="table_65CF778F5BDA45118208538DCBE203FB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura  </span> </p> </td> 
   <td colname="col2"> <p>Compartilhar largura do link. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir o link de compartilhamento como 450 pixels de largura:

```
.s7videoviewer .s7linkdialog .s7dialoglink { 
    width: 450px; 
}
```

