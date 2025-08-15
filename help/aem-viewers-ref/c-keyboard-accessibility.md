---
title: Acessibilidade e navegação pelo teclado
description: Todos os recursos expostos na interface de visualização Basic Zoom, eCatalog, eCatalog Search, Flyout, Inline Zoom, Mixed Media, Spin, Video, Zoom, Dimensional (3D), Carousel, Interative Image, Interative Video e Video360 são acessíveis pelo teclado.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 0bdf172a-0bde-42d2-900f-f207538fe588
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 0%

---

# Acessibilidade e navegação pelo teclado{#keyboard-accessibility-and-navigation}

Todos os recursos expostos nas interfaces de visualização Basic Zoom, eCatalog, eCatalog Search, Flyout, Inline Zoom, Mixed Media, Spin, Video, Zoom, Carousel, Dimensional (3D), Interative Image, Interative Video e Video360 são acessíveis pelo teclado.

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Acessibilidade e navegação pelo teclado {#topic-f5650e9493404e55a3627c8d1366b861}

Todos os recursos expostos nas interfaces de visualização Basic Zoom, eCatalog, eCatalog Search, Flyout, Inline Zoom, Mixed Media, Spin, Video, Zoom, Carousel, Dimensional (3D), Interative Image, Interative Video e Video360 são acessíveis pelo teclado.

Um usuário final pode navegar entre os elementos da interface do usuário do visualizador usando **[!UICONTROL Tab]** e **[!UICONTROL Shift+Tab]** pressionamentos de teclas. O uso de **[!UICONTROL Tab]** avança o foco de entrada para o próximo elemento da interface do usuário na ordem de tabulação; o uso de **[!UICONTROL Shift+Tab]** traz o foco de entrada de volta para o elemento da interface do usuário anterior. O percurso do foco segue o local natural do elemento da interface do usuário na tela e se move da esquerda para a direita e de cima para baixo.

Dependendo das configurações do sistema operacional e do navegador da Web, o elemento da interface do usuário com foco de entrada recebe uma indicação de foco visual. Por exemplo, o indicador visual pode ser uma borda fina renderizada ao redor do elemento da interface do usuário.

É possível desativar ou personalizar esse destaque de foco no CSS do visualizador. No índice deste sistema de Ajuda, sob um nome de visualizador específico (por exemplo, Zoom básico ou Vídeo interativo), clique em **Personalizando o *nome do visualizador*** >** Focalizar destaque **.

Os pressionamentos de tecla suportados por elementos da interface do usuário do visualizador individual são, na maioria dos casos, óbvios e fáceis de descobrir.

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Ação </p> </th> 
   <th colname="col2" class="entry"> <p>Pressionamento de tecla </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Ativar componentes do botão </p> </td> 
   <td colname="col2"> <p>Espaço ou tecla Enter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aumentar ou diminuir o zoom </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> + </span> ou <span class="uicontrol"> - </span>, respectivamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Restaurar zoom </p> </td> 
   <td colname="col2"> <p>Esc key. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Panorâmica </p> </td> 
   <td colname="col2"> <p>Teclas de seta para cima, para baixo, para a esquerda ou para a direita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Girar uma imagem de 360 graus </p> </td> 
   <td colname="col2"> <p>Use as teclas de seta quando a imagem estiver em um estado redefinido. </p> <p>Use as teclas de seta para cima ou para baixo ao trabalhar com conjuntos de rotação multidimensionais. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Seleção da amostra do produto </p> </td> 
   <td colname="col2"> <p>Tecla de seta para cima, para baixo, para a esquerda ou para a direita; tecla Home ou End. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ativação de amostra de produto </p> </td> 
   <td colname="col2"> <p>Espaço ou tecla Enter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo e vídeo interativo, retrocesso gradual </p> </td> 
   <td colname="col2"> <p>Seta para a esquerda ou para cima. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo e vídeo interativo, avançar rapidamente </p> </td> 
   <td colname="col2"> <p>Tecla de seta para a direita ou para baixo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo e Vídeo Interativo, vá para o início ou fim </p> </td> 
   <td colname="col2"> <p>Chave inicial ou final, respectivamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo e Vídeo Interativo, controle o nível do volume quando o foco está no controle deslizante </p> </td> 
   <td colname="col2"> <p>Tecla de seta para cima, para baixo, para a esquerda ou para a direita; tecla Home ou End. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo e Vídeo interativo, volume mutável </p> </td> 
   <td colname="col2"> <p>Teclas de seta, Início e Fim para controlar o nível do volume quando o foco está na parte deslizante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vídeo, quando a caixa de diálogo modal é exibida, a passagem do foco se limita somente aos controles da caixa de diálogo. </p> </td> 
   <td colname="col2"> <p>Esc key para fechar a caixa de diálogo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carrossel, alterar imagem do banner na exibição principal </p> </td> 
   <td colname="col2"> <p>Tecla de seta para a esquerda ou direita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carrossel, seleção de pontos de acesso e ativação de pontos de acesso </p> </td> 
   <td colname="col2"> <p>Seleção do ponto de acesso: tecla de seta para cima, para baixo, para a esquerda ou para a direita </p> <p>Ativação do ponto de acesso: tecla Space ou Enter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, altere a imagem da página na exibição principal </p> </td> 
   <td colname="col2"> <p> Teclas de seta para a esquerda ou direita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, seleção de miniatura </p> </td> 
   <td colname="col2"> <p>Teclas de seta; teclas Home e End. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, ativação de amostra </p> </td> 
   <td colname="col2"> <p>Espaço ou tecla Enter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, seleção de pontos de acesso </p> </td> 
   <td colname="col2"> <p>Teclas de seta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, ativação </p> </td> 
   <td colname="col2"> <p>Teclas Space ou Enter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, ativação de componentes suspensos </p> </td> 
   <td colname="col2"> <p> Tecla de seta para baixo; tecla Espaço ou tecla Enter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, quando o foco está no painel suspenso </p> </td> 
   <td colname="col2"> <p>Use as teclas de seta para selecionar um item específico no painel antes de ativá-lo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, quando uma caixa de diálogo modal é exibida, a passagem do foco fica limitada somente aos controles da caixa de diálogo. </p> </td> 
   <td colname="col2"> <p>Esc key para fechar a caixa de diálogo. </p> </td> 
  </tr> 
 </tbody> 
</table>
