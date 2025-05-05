---
title: Incorporar compartilhamento
description: A ferramenta de compartilhamento incorporada consiste em um botão adicionado ao painel Compartilhamento em redes sociais e à caixa de diálogo modal exibida quando a ferramenta é ativada. A posição do botão é totalmente gerenciada pela ferramenta Compartilhamento em redes sociais.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: d5f8db82-f1f9-45be-990d-ebfef97507b6
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '2621'
ht-degree: 0%

---

# Incorporar compartilhamento{#embed-share}

A ferramenta de compartilhamento incorporada consiste em um botão adicionado ao painel Compartilhamento em redes sociais e à caixa de diálogo modal exibida quando a ferramenta é ativada. A posição do botão é totalmente gerenciada pela ferramenta Compartilhamento em redes sociais.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

A aparência do botão de compartilhamento incorporado é controlada com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embedshare
```

**Propriedades CSS da ferramenta de compartilhamento de inserção**

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
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão oferece suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

É possível remover o botão do painel Compartilhamento em redes sociais definindo a propriedade CSS `display:none` em sua classe CSS.

A dica de ferramenta do botão pode ser localizada. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obter mais informações.

Exemplo - Para configurar um botão Incorporar compartilhamento com 28 x 28 pixels e exibir uma imagem diferente para cada um dos quatro estados de botão diferentes:

```
.s7smartcropvideoviewer .s7embedshare { 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7embedshare[state='up'] { 
background-image:url(images/v2/EmbedShare_dark_up.png); 
} 
.s7smartcropvideoviewer .s7embedshare[state='over'] { 
background-image:url(images/v2/EmbedShare_dark_over.png); 
} 
.s7smartcropvideoviewer .s7embedshare[state='down'] { 
background-image:url(images/v2/EmbedShare_dark_down.png); 
} 
.s7smartcropvideoviewer .s7embedshare[state='disabled'] { 
background-image:url(images/v2/EmbedShare_dark_disabled.png); 
}
```

A sobreposição de plano de fundo que cobre a página da Web quando a caixa de diálogo está ativa é controlada com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7backoverlay
```

**Propriedades CSS da sobreposição de plano de fundo**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacidade </span> </p> </td> 
   <td colname="col2"> <p>Opacidade de sobreposição de plano de fundo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>Cor de sobreposição do plano de fundo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma sobreposição de plano de fundo para ficar cinza com 70% de opacidade:

```
.s7smartcropvideoviewer .s7embeddialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Por padrão, a caixa de diálogo modal é exibida centralizada na tela em sistemas desktop e ocupa toda a área da página da Web em dispositivos de toque. Em todos os casos, o posicionamento e o dimensionamento da caixa de diálogo são gerenciados pelo componente. A caixa de diálogo é controlada com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialog
```

**Propriedades CSS da caixa de diálogo**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> raio da borda </span> </p> </td> 
   <td colname="col2"> <p> Raio da borda da caixa de diálogo, caso a caixa de diálogo não use todo o navegador. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>Cor de fundo da caixa de diálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Deve ser desdefinido ou definido como 100%, nesse caso, a caixa de diálogo usa toda a janela do navegador (esse modo é preferível em dispositivos de toque). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Deve ser desdefinido ou definido como 100%, nesse caso, a caixa de diálogo usa toda a janela do navegador (esse modo é preferível em dispositivos de toque). </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar a caixa de diálogo para usar toda a janela do navegador e ter um fundo branco em dispositivos de toque:

```
.s7smartcropvideoviewer .s7touchinput .s7embeddialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

O cabeçalho da caixa de diálogo consiste em um ícone, um texto de título e um botão Fechar. O contêiner de cabeçalho é controlado com

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogheader
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
.s7smartcropvideoviewer .s7embeddialog .s7dialogheader .s7dialogline
```

**Propriedades CSS da linha de diálogo**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p> Preenchimento interno para o ícone e título do cabeçalho </p> </td> 
  </tr> 
 </tbody> 
</table>

O ícone de cabeçalho é controlado com o seguinte seletor de classe CSS

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogheadericon
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
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

O título do cabeçalho é controlado com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogheadertext
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
.s7smartcropvideoviewer .s7embeddialog .s7closebutton
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
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Este botão oferece suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

A dica de ferramenta do botão Fechar e o título da caixa de diálogo podem ser localizados. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obter mais informações.

Exemplo - Para configurar um cabeçalho de caixa de diálogo com preenchimento, ícone de 24 x 14 pixels, título em negrito de 16 pontos e um botão Fechar de 28 x 28 pixels. Por fim, posicione-o a dois pixels da parte superior e a dois pixels da direita do contêiner da caixa de diálogo:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogheader { 
 padding: 10px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgembed_cap.png"); 
    height: 14px; 
    width: 24px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

O rodapé da caixa de diálogo consiste no botão &quot;cancelar&quot;. O contêiner de rodapé é controlado com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogfooter
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

O rodapé tem um contêiner interno que mantém o botão. Ele é controlado com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogbuttoncontainer
```

**Propriedades CSS do contêiner de botão da caixa de diálogo**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p> Preenchimento interno entre o rodapé e o botão. </p> </td> 
  </tr> 
 </tbody> 
</table>

O botão Selecionar tudo é controlado com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogactionbutton
```

O botão só está disponível em sistemas desktop.

**Propriedades CSS do botão Selecionar Tudo**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
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
>O botão Selecionar tudo oferece suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

O botão Cancelar é controlado com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogcancelbutton
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
>O botão Cancelar oferece suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

Além disso, ambos os botões compartilham uma classe CSS comum, que pode conter configurações CSS que são as mesmas para outros botões da caixa de diálogo:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogfooter .s7button
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

As dicas de ferramentas do botão podem ser localizadas. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obter mais informações.

Exemplo - para configurar um rodapé de caixa de diálogo com um botão Cancelar 64 x 34, com cores de texto e cores de plano de fundo diferentes para cada estado de botão:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

A área de diálogo principal, entre o cabeçalho e o rodapé, contém conteúdo de diálogo rolável e painel de rolagem à direita. Em todos os casos, o componente gerencia a largura dessa área. Não é possível defini-la no CSS. A área de diálogo principal é controlada com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogviewarea
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

Exemplo - para configurar uma área da caixa de diálogo principal com altura de 300 pixels, ter uma margem de dez pixels e usar um plano de fundo branco:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

Todo o conteúdo do formulário (como rótulos e campos de entrada) reside dentro de um container controlado com

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogbody
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

Exemplo - Para configurar o conteúdo do formulário para ter um preenchimento de dez pixels:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogbody { 
    padding: 10px; 
}
```

Todos os rótulos estáticos no formulário da caixa de diálogo são controlados com

```
.s7smartcropvideoviewer .s7embeddialog .s7dialoglabel
```

Essa classe não é adequada para controlar o tamanho ou a posição do rótulo porque você pode aplicá-la a textos em vários locais da interface do usuário do formulário.

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

As dicas de ferramentas dos rótulos da caixa de diálogo podem ser localizadas. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obter mais informações.

Exemplo - para configurar todos os rótulos para serem cinza, negrito com uma fonte de nove pixels:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

O tamanho da cópia de texto exibida na parte superior do código incorporado é controlado com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialoginputwide
```

**Propriedades CSS do campo de entrada da caixa de diálogo**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do campo de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir a cópia de texto como 430 pixels de largura e ter um preenchimento de dez pixels na parte inferior:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

O código incorporado é colocado em um container e controlado com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialoginputcontainer
```

**Propriedades CSS do contêiner de entrada da caixa de diálogo**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>A largura do contêiner do código de inserção. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borda </span> </p> </td> 
   <td colname="col2"> <p>Borda ao redor do contêiner do código de inserção. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir uma borda cinza de um pixel em torno do texto do código incorporado, torne-o com 430 pixels de largura e tenha um preenchimento de dez pixels:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 10px; 
    width: 430px; 
}
```

O texto real do código incorporado é controlado com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialoginputcontainer
```

**Propriedades CSS do contêiner de entrada da caixa de diálogo**

<table id="table_FEEF66150C69489BB42A2408EBFCE928"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> quebra automática de linha </span> </p> </td> 
   <td colname="col2"> <p>Estilo de quebra de linha. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - Para configurar o código de inserção para usar a quebra automática de linha `break-word`:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogmessage { 
    word-wrap: break-word; 
}
```

O rótulo de tamanho incorporado e o menu suspenso estão na parte inferior da caixa de diálogo e são colocados em um container controlado com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogembedsizepanel
```

**Propriedades CSS do painel de tamanho incorporado da caixa de diálogo**

<table id="table_6BA2769361BA4EC4AB7D250EC9486CB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p>Preenchimento interno. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um painel de tamanho incorporado com dez pixels de preenchimento:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogembedsizepanel { 
    padding: 10px; 
}
```

O tamanho e o alinhamento do rótulo de tamanho incorporado são controlados com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogembedsizepanel
```

**Propriedades CSS do painel de tamanho incorporado da caixa de diálogo**

<table id="table_8E50C63C9B1349999251CDB5E5AD3D1D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> alinhamento vertical </span> </p> </td> 
   <td colname="col2"> <p>Alinhamento vertical do rótulo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do rótulo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir o rótulo do tamanho incorporado como alinhado na parte superior e com 80 pixels de largura:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogembedsizelabel { 
    vertical-align: top; 
    width: 80px; 
}
```

A largura da caixa de combinação de tamanho incorporado é controlada com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7combobox
```

**Propriedades CSS da caixa de combinação**

<table id="table_C0FEA0C7353F40039204641BB3F1AE14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura da caixa de combinação. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>A caixa de combinação dá suporte ao seletor de atributos `expanded` com valores possíveis de `true` e `false`. O valor `true` é usado quando a caixa de combinação exibe um dos tamanhos incorporados predefinidos, portanto deve ter toda a largura disponível. O valor `false` é usado quando a opção de tamanho personalizado é selecionada na caixa de combinação; portanto, ele deve ser reduzido para permitir espaço para campos de entrada personalizados de largura e altura.

Exemplo - para definir a caixa de combinação de tamanho incorporado como 300 pixels de largura ao mostrar um item predefinido e 110 pixels de largura ao mostrar um tamanho personalizado:

```
.s7smartcropvideoviewer .s7embeddialog .s7combobox[expanded="true"] { 
    width: 300px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7combobox[expanded="false"] { 
    width: 110px; 
}
```

A altura do texto da caixa de combinação é definida por um elemento interno especial e é controlada com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxtext
```

**Propriedades CSS do texto da caixa de combinação**

<table id="table_AB60032BF337433F8455DE20AFBA29AB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do texto da caixa de combinação. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir a altura do texto da caixa de combinação de tamanho incorporado como 40 pixels:

```
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxtext { 
    height: 40px; 
}
```

A caixa de combinação tem um botão &quot;suspenso&quot; à direita e é controlada com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxbutton
```

**Propriedades CSS do botão de caixa de combinação**

<table id="table_70E127FA21264366AD5DBBD7DF40EBAA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Posição vertical do botão dentro da caixa de combinação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> direita </span> </p> </td> 
   <td colname="col2"> <p>Posição do botão horizontal dentro da caixa de combinação. </p> </td> 
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
   <td colname="col2"> <p>Imagem do botão para cada estado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Este botão oferece suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes.

Exemplo - para definir um botão &quot;suspenso&quot; como 28 x 28 pixels e ter uma imagem separada para cada estado:

```
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxbutton { 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='up'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='over'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='down'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='disabled'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
}
```

O painel com a lista de tamanhos incorporados exibidos quando a caixa de combinação é aberta é controlado com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7comboboxdropdown
```

O tamanho e a posição do painel são controlados pelo componente. Não é possível alterá-lo por meio do CSS.

**Propriedades CSS do menu suspenso da caixa de combinação**

<table id="table_FA7345321C6A4E63B4B78ECF81CE18DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borda </span> </p> </td> 
   <td colname="col2"> <p>Borda do painel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir o painel da caixa de combinação para ter uma borda cinza de um pixel:

```
.s7smartcropvideoviewer .s7embeddialog .s7comboboxdropdown { 
    border: 1px solid #CCCCCC; 
}
```

Um único item em um painel suspenso que é controlado com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dropdownitemanchor
```

**Propriedades CSS da âncora do item suspenso**

<table id="table_FD42FDD56F89463A97FD292FAA04DA5A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p>Plano de fundo do item. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir o item do painel da caixa de combinação para ter um plano de fundo branco:

```
.s7smartcropvideoviewer .s7embeddialog .s7dropdownitemanchor { 
    background-color: #FFFFFF; 
}
```

Uma marca de seleção exibida à esquerda do item selecionado dentro do painel da caixa de combinação que é controlado com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7checkmark
```

**Propriedades CSS da caixa de seleção**

<table id="table_8E01F5461CD04AC18B2C3725A961476A"> 
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
   <td colname="col2"> <p>Imagem do item. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir o ícone de marca de seleção como 25 x 25 pixels:

```
.s7smartcropvideoviewer .s7embeddialog .s7checkmark { 
    background-image: url("images/sdk/cboxchecked.png"); 
    height: 25px; 
    width: 25px; 
}
```

Quando a opção &quot;Tamanho personalizado&quot; está selecionada na caixa de combinação de tamanho incorporado, a caixa de diálogo exibe dois campos de entrada adicionais à direita para permitir que o usuário insira um tamanho incorporado personalizado. Esses campos são envolvidos em um container controlado com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogcustomsizepanel
```

**Propriedades CSS do painel de tamanho personalizado da caixa de diálogo**

<table id="table_B00829EA550F4E5E8F51B1C6ADACCD34"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> saiu de </span> </p> </td> 
   <td colname="col2"> <p> Distância da caixa de combinação de tamanho incorporado. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir o painel de campos de entrada de tamanho personalizado como 20 pixels à direita da caixa de combinação:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogcustomsizepanel { 
    left: 20px; 
}
```

Cada campo de entrada de tamanho personalizado é colocado em um container que renderiza uma borda e define a margem entre os campos. Ele é controlado com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogcustomsize
```

**Propriedades CSS do tamanho personalizado da caixa de diálogo**

<table id="table_A8A04BE1988641618D0A412B8AEEE1C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> borda </span> </p> </td> 
   <td colname="col2"> <p>Borda ao redor do campo de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p> Largura do campo de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margem </span> </p> </td> 
   <td colname="col2"> <p> Margem do campo de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento </span> </p> </td> 
   <td colname="col2"> <p> Preenchimento do campo de entrada. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para definir os campos de entrada de tamanho personalizado para ter uma borda cinza de um pixel, margem, preenchimento e ter 70 pixels de largura:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogcustomsize { 
    border: 1px solid #CCCCCC; 
    margin-right: 20px; 
    padding-left: 2px; 
    padding-right: 2px; 
    width: 70px; 
}
```

Se a rolagem vertical for necessária, a barra de rolagem será renderizada no painel próximo à borda direita da caixa de diálogo, que é controlada com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogscrollpanel
```

**Propriedades CSS do painel de rolagem da caixa de diálogo**

<table id="table_BA37E577E0884C919383F84080E2DD28"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura do painel de rolagem </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar um painel de rolagem com 44 pixels de largura

```
.s7smartcropvideoviewer .s7embeddialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

A aparência da área da barra de rolagem é controlada com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar
```

**Propriedades CSS da barra de rolagem**

<table id="table_066492417FCA43929017993D7326CDB8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura da barra de rolagem </p> </td> 
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

Exemplo - para configurar uma barra de rolagem com 28 pixels de largura e uma margem de oito pixels na parte superior, direita e inferior do painel de rolagem:

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

A faixa da barra de rolagem é a área entre os botões de rolagem superior e inferior. O componente define automaticamente a posição e a altura da faixa. A faixa é controlada com o seguinte seletor de classe CSS

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolltrack
```

**Propriedades CSS da faixa de barra de rolagem**

<table id="table_19CF5503C1D34ED9998D4F4A6DA7D5D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura da faixa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cor de fundo </span> </p> </td> 
   <td colname="col2"> <p> Cor do plano de fundo da faixa. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exemplo - para configurar uma faixa de barra de rolagem com 28 pixels de largura e um plano de fundo cinza:

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

A miniatura da barra de rolagem se move verticalmente em uma área de rastreamento de rolagem. Sua posição vertical é totalmente controlada pela lógica do componente. No entanto, a altura da miniatura não muda dinamicamente, dependendo da quantidade de conteúdo. A altura da miniatura e outros aspectos podem ser configurados com o seguinte seletor de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollthumb
```

**Propriedades CSS da miniatura da barra de rolagem**

<table id="table_90BC468FE138441C9DBAB1EB109F3DB0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> largura </span> </p> </td> 
   <td colname="col2"> <p>Largura da miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altura </span> </p> </td> 
   <td colname="col2"> <p>Altura do polegar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top </span> </p> </td> 
   <td colname="col2"> <p>O preenchimento vertical entre o topo da faixa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> preenchimento inferior </span> </p> </td> 
   <td colname="col2"> <p> O preenchimento vertical entre a parte inferior da faixa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imagem de fundo </span> </p> </td> 
   <td colname="col2"> <p> A imagem exibida para um determinado estado de miniatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>A miniatura dá suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de miniatura diferentes: `up`, `down`, `over` e `disabled`.

Exemplo - para configurar uma miniatura de barra de rolagem com 28 x 45 pixels, tem uma margem de dez pixels na parte superior e inferior e tem um trabalho artístico diferente para cada estado:

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

A aparência dos botões de rolagem superior e inferior é controlada com os seguintes seletores de classe CSS:

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton 
```

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton
```

Não é possível posicionar botões de rolagem usando as propriedades CSS top, left, bottom e right. Em vez disso, a lógica do visualizador as posiciona automaticamente.

**Propriedades CSS dos botões de rolagem superior e inferior**

<table id="table_554BFCFEAF4F43A9AE5F741DC126F833"> 
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
   <td colname="col2"> <p> Posicionar dentro da imagem de arte-final, se as imagens CSS forem usadas. </p> <p>Consulte <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprites CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Estes botões oferecem suporte ao seletor de atributos `state`, que pode ser usado para aplicar capas diferentes a estados de botão diferentes: `up`, `down`, `over` e `disabled`.

As dicas de ferramentas do botão podem ser localizadas. Consulte [Localização dos elementos da interface do usuário](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) para obter mais informações.

Exemplo - para configurar botões de rolagem com 28 x 32 pixels e que tenham arte-final diferente para cada estado:

```
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7smartcropvideoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```
