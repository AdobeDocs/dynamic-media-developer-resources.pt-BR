---
description: Todos os recursos expostos na interface do visualizador Zoom básico, eCatalog, eCatalog Search, Flyout, Zoom em linha, Mídia mista, Rotação, Vídeo, Zoom, Dimensional (3D), Carrossel, Imagem interativa, Vídeo interativo e Vídeo360 são acessíveis pelo teclado.
solution: Experience Manager
title: Acessibilidade e navegação do teclado
feature: Dynamic Media Classic,Visualizadores,SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 0%

---


# Acessibilidade e navegação do teclado{#keyboard-accessibility-and-navigation}

Todos os recursos expostos na interface do visualizador Zoom básico, eCatalog, eCatalog Search, Flyout, Zoom em linha, Mídia mista, Rotação, Vídeo, Zoom, Carrossel, Dimensional (3D), Imagem interativa, Vídeo interativo e Vídeo360 são acessíveis pelo teclado.

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Acessibilidade e navegação do teclado {#topic-f5650e9493404e55a3627c8d1366b861}

Todos os recursos expostos na interface do visualizador Zoom básico, eCatalog, eCatalog Search, Flyout, Zoom em linha, Mídia mista, Rotação, Vídeo, Zoom, Carrossel, Dimensional (3D), Imagem interativa, Vídeo interativo e Vídeo360 são acessíveis pelo teclado.

Um usuário final pode navegar entre os elementos da interface do usuário do visualizador usando **[!UICONTROL Tab]** e **[!UICONTROL Shift+Tab]** pressionamentos de teclas. Usar **[!UICONTROL Tab]** avança o foco de entrada para o próximo elemento da interface do usuário na ordem de tabulação; usar **[!UICONTROL Shift+Tab]** traz o foco de entrada de volta ao elemento anterior da interface do usuário. A travessia de foco segue a localização do elemento da interface de usuário natural na tela e se move de esquerda para direita e de cima para baixo.

Dependendo das configurações do sistema operacional e do navegador da Web, o elemento da interface do usuário que tem foco de entrada pode receber uma indicação de foco visual. Por exemplo, o indicador visual pode ser uma borda fina renderizada em torno do elemento da interface do usuário.

É possível desativar ou personalizar esse realce de foco no CSS do visualizador. No índice deste sistema de Ajuda, em um nome de visualizador específico (por exemplo, Zoom básico ou Vídeo interativo), clique em **Personalizando *nome do visualizador*** >** Destaque do foco **.

Os pressionamentos de tecla suportados por elementos da interface do visualizador individual são, na maioria dos casos, óbvios e fáceis de descobrir.

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Ação </p> </th> 
   <th colname="col2" class="entry"> <p>Tecla </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Ativar componentes do botão </p> </td> 
   <td colname="col2"> <p>Tecla Space ou Enter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aumentar ou diminuir o zoom </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> +  </span> ou  <span class="uicontrol"> -  </span>, respectivamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Redefinição de zoom </p> </td> 
   <td colname="col2"> <p>Chave Esc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Panorâmica </p> </td> 
   <td colname="col2"> <p>Tecla de seta para cima, para baixo, para a esquerda ou para a direita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rodar uma imagem de 360 graus </p> </td> 
   <td colname="col2"> <p>Use as teclas de seta quando a imagem estiver em um estado de redefinição. </p> <p>Use a tecla de seta para cima ou para baixo ao trabalhar com conjuntos de rotação multidimensional. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Seleção da amostra de produto </p> </td> 
   <td colname="col2"> <p>Tecla de seta para cima, para baixo, para a esquerda ou para a direita; Chave inicial ou final. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ativação da amostra de produto </p> </td> 
   <td colname="col2"> <p>Tecla Space ou Enter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo e Vídeo interativo, retrocesso gradual </p> </td> 
   <td colname="col2"> <p>Tecla de seta para a esquerda ou para cima. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo e vídeo interativo, avançar rapidamente </p> </td> 
   <td colname="col2"> <p>Tecla de seta para a direita ou para baixo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo e Vídeo interativo, vá para o início ou fim </p> </td> 
   <td colname="col2"> <p>Chave inicial ou final, respectivamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo e Vídeo interativo, controle o nível do volume quando o foco estiver no controle deslizante </p> </td> 
   <td colname="col2"> <p>Tecla de seta para cima, para baixo, para a esquerda ou para a direita; Chave inicial ou final. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo e Vídeo interativo, volume mutável </p> </td> 
   <td colname="col2"> <p>Teclas de seta, início e fim para controlar o nível do volume quando o foco estiver na parte do controle deslizante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo, quando a caixa de diálogo modal é exibida, a travessia do foco fica limitada somente aos controles da caixa de diálogo. </p> </td> 
   <td colname="col2"> <p>Chave Esc para fechar a caixa de diálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carrossel, alterar a imagem do banner na exibição principal </p> </td> 
   <td colname="col2"> <p>Tecla de seta para a esquerda ou para a direita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carrossel, seleção de ponto de conexão e ativação de ponto de conexão </p> </td> 
   <td colname="col2"> <p>Seleção de ponto de acesso: tecla de seta para cima, para baixo, para a esquerda ou para a direita </p> <p>Ativação de ponto de acesso: Tecla Space ou Enter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo eletrônico, altere a imagem da página na exibição principal </p> </td> 
   <td colname="col2"> <p> Teclas de seta para a esquerda ou para a direita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo eletrônico, seleção de miniatura </p> </td> 
   <td colname="col2"> <p>Teclas de seta; Chave inicial e final. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo eletrônico, ativação de amostra </p> </td> 
   <td colname="col2"> <p>Tecla Space ou Enter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo eletrônico, seleção de ponto de acesso </p> </td> 
   <td colname="col2"> <p>Teclas de seta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo eletrônico, ativação </p> </td> 
   <td colname="col2"> <p>Teclas Space ou Enter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo eletrônico, ativação de componentes suspensos </p> </td> 
   <td colname="col2"> <p> Tecla de seta para baixo; Espaço ou tecla Enter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo eletrônico, quando o foco está no painel suspenso </p> </td> 
   <td colname="col2"> <p>Use as teclas de seta para selecionar um item específico no painel antes de ativá-lo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catálogo eletrônico, quando uma caixa de diálogo modal é exibida, a travessia do foco fica limitada somente aos controles da caixa de diálogo. </p> </td> 
   <td colname="col2"> <p>Chave Esc para fechar a caixa de diálogo. </p> </td> 
  </tr> 
 </tbody> 
</table>

