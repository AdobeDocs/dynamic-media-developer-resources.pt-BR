---
description: A Biblioteca de imagens responsiva é um módulo JavaScript que ajusta dinamicamente a qualidade de imagens veiculadas no Dynamic Media e incorporadas em páginas da Web responsivas. Além disso, oferece qualidade de imagem aprimorada em dispositivos com telas de alta densidade. A biblioteca também pode renderizar com agilidade os resultados do Recorte inteligente e do Recorte inteligente.
solution: Experience Manager
title: Sobre a biblioteca de imagens responsiva
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f853b9b4-917c-4744-b2a5-25fde2532356
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# Sobre a biblioteca de imagens responsiva{#about-responsive-image-library}

A Biblioteca de imagens responsiva é um módulo JavaScript que ajusta dinamicamente a qualidade de imagens veiculadas no Dynamic Media e incorporadas em páginas da Web responsivas. Além disso, oferece qualidade de imagem aprimorada em dispositivos com telas de alta densidade. A biblioteca também pode renderizar com agilidade os resultados do Recorte inteligente e do Recorte inteligente.

## URLs de demonstração {#section-4f72c1dc38bf4e03acfa5205733a05a5}

O caso de uso mais simples da Biblioteca de imagens responsiva é definir uma lista de valores de pontos de interrupção para a largura da imagem. Essa lista garante que a representação apropriada seja carregada e exibida quando uma imagem for redimensionada devido a alterações no layout da página da Web feitas por um usuário ao redimensionar a janela do navegador ou alterar a orientação do dispositivo. A biblioteca monitora continuamente o tamanho da imagem na tela e, sempre que uma nova largura de ponto de interrupção é atingida, ela obtém uma nova representação de imagem da Dynamic Media.

<table id="table_3D3D3991B802461A888E1093C1217D26"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>URL de demonstração </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html" scope="external" format="https"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>Este é um exemplo simples onde a imagem responsiva está dentro de um container que ocupa 50% da largura da página da Web. Toda vez que a janela do navegador é redimensionada, a largura do contêiner muda. Quando a largura da imagem atinge um dos pontos de interrupção configurados, que são definidos como 200, 400, 600 e 800 pixels para fins ilustrativos, uma nova representação é baixada e exibida. O objetivo é evitar o carregamento de imagens grandes desnecessárias e economizar largura de banda na rede. </p> <p>Clique no URL para abrir a página da Web, redimensionar a janela do navegador e monitorar o tráfego de rede. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>O exemplo de Bootstrap a seguir ilustra o mesmo caso de uso em uma página da Web. De acordo com o Bootstrap CSS, a célula de layout à qual a imagem responsiva é adicionada pode ter uma das seguintes larguras: 360, 720 e 940 pixels. Esses valores são exatamente os que são passados como pontos de interrupção para a Biblioteca de imagens responsiva. Dessa forma, a Dynamic Media garante que a largura de banda da rede do cliente seja usada com eficiência. Além disso, também garante que a imagem seja exibida no tamanho exato necessário, considerando o layout da página da Web atual, sem que nenhum artefato visual seja dimensionado no navegador do lado do cliente. </p> <p>Clique no URL para abrir a página da Web, redimensione a janela do navegador para obter diferentes pontos de interrupção de layout e monitorar o tráfego de rede. </p> <p>Casos de uso mais avançados incluem a associação de diferentes Predefinições de imagem, comandos do Servidor de imagens, ou ambos, a diferentes valores de ponto de interrupção. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html</a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>Neste próximo exemplo, são usadas Predefinições de imagem de qualidade e formato de imagem diferentes para tamanhos de pontos de interrupção diferentes. Para um ponto de interrupção pequeno, uma predefinição de baixa qualidade é aplicada, o que força o Servidor de imagens a retornar a imagem de GIF compactada somente para seis cores. Um ponto de interrupção médio está usando uma Predefinição de imagem configurada para JPEG com alta compactação. O maior ponto de interrupção está associado a uma predefinição de imagem de alta qualidade usando PNG sem perdas. Esse método garante que imagens de alta qualidade sejam entregues a esses dispositivos, com base no pressuposto de que dispositivos com telas maiores têm maior largura de banda e poder de processamento. </p> <p>Clique no URL para abrir a página da Web, redimensione a janela do navegador da Web de maior para menor e observe como a qualidade da imagem diminui. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>Além das Predefinições de imagem, é possível associar comandos específicos do Servidor de imagens a pontos de interrupção. O exemplo a seguir mostra como é possível cortar gradualmente a imagem do banner na região de interesse à medida que o tamanho da imagem na tela se torna menor. Aqui, o maior ponto de interrupção não tem comandos do Servidor de imagens, portanto, a imagem do banner é totalmente visível. No ponto de interrupção médio aplica corte moderado, tornando visível apenas o executor com o texto "Em execução". Em um ponto de interrupção pequeno, mais cortes são aplicados para que somente o produto seja exibido. </p> <p>Clique no URL para abrir a página da Web e redimensionar a janela do navegador. Observe como a imagem corta gradualmente à medida que passa de um tamanho maior para um menor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>Você também pode usar os comandos do Servidor de imagens com os Modelos de servidor de imagens para controlar determinados parâmetros de modelo com base no tamanho da imagem. Neste próximo exemplo, um modelo de disponibilização de imagens é usado, onde o tamanho da fonte da sobreposição de texto é parametrizado com o uso de <span class="codeph"> $fontsize </span> parâmetro. A imagem responsiva é configurada para usar um tamanho de fonte maior para tamanhos de imagem menores para garantir que o texto sempre permaneça legível: </p> </td> 
  </tr> 
 </tbody> 
</table>

## Requisitos do sistema {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**Hardware e software do servidor**

* Dynamic Media Image Serving 6.0.1 ou posterior.

**Requisitos mínimos do navegador do cliente**

* Microsoft® Windows® 7 ou posterior; macOS X 10.8 ou posterior.
* Firefox 23, Safari 6, Chrome 29, IE 9 ou posterior.
* iOS 6 ou posterior.
* Certificado no iPhone3GS ou posterior e iPad2 ou posterior (somente navegadores nativos).
* Android™ OS 2.3 ou posterior.
* O Internet Explorer em dispositivos móveis não é suportado atualmente.
