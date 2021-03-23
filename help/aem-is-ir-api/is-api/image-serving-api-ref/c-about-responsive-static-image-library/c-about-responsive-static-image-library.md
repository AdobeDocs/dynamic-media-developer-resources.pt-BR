---
description: A Biblioteca de imagens responsivas é um módulo JavaScript que ajusta dinamicamente a qualidade das imagens fornecidas pelo Dynamic Media e incorporadas a páginas responsivas da Web. Além disso, ele fornece qualidade de imagem aprimorada em dispositivos com telas de alta densidade. A biblioteca também pode renderizar resultados de forma responsiva do Recorte inteligente e da Amostra inteligente.
solution: Experience Manager
title: Sobre a biblioteca de imagens responsivas
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '925'
ht-degree: 0%

---


# Sobre a biblioteca de imagens responsivas{#about-responsive-image-library}

A Biblioteca de imagens responsivas é um módulo JavaScript que ajusta dinamicamente a qualidade das imagens fornecidas pelo Dynamic Media e incorporadas a páginas responsivas da Web. Além disso, ele fornece qualidade de imagem aprimorada em dispositivos com telas de alta densidade. A biblioteca também pode renderizar resultados de forma responsiva do Recorte inteligente e da Amostra inteligente.

## URLs de demonstração {#section-4f72c1dc38bf4e03acfa5205733a05a5}

O caso de uso mais simples da Biblioteca de imagens responsivas é definir uma lista de valores de ponto de interrupção para a largura da imagem. Essa lista garante que a representação apropriada seja carregada e exibida quando uma imagem for redimensionada devido ao layout da página da Web mudar de um usuário que redimensiona a janela do navegador ou altera a orientação do dispositivo. A biblioteca monitora continuamente o tamanho da imagem na tela e, sempre que uma nova largura de ponto de interrupção é atingida, ela obtém uma nova representação de imagem do Dynamic Media.

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
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html" scope="external" format="https"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>A seguir, um exemplo simples em que a imagem responsiva está em um contêiner que utiliza 50% da largura da página da Web. Toda vez que a janela do navegador é redimensionada, a largura do contêiner muda. Quando a largura da imagem atinge um dos pontos de interrupção configurados, que são definidos em 200, 400, 600 e 800 pixels para fins ilustrativos, uma nova renderização é baixada e exibida. O objetivo é evitar o carregamento de imagens grandes desnecessárias e economizar largura de banda da rede. </p> <p>Clique no URL para abrir a página da Web, redimensionar a janela do navegador e monitorar o tráfego da rede. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>O exemplo de Bootstrap a seguir ilustra o mesmo caso de uso em uma página da Web. De acordo com o CSS do Bootstrap, a célula de layout à qual a imagem responsiva é adicionada pode ter uma das seguintes larguras: 360, 720 e 940 pixels. Esses são os valores exatos que são passados como pontos de interrupção para a Biblioteca de imagens responsivas. Dessa forma, a Dynamic Media garante que a largura de banda da rede do cliente seja usada de forma eficaz. Além disso, garante que a imagem seja exibida no tamanho exato necessário, dado o layout atual da página da Web, sem que nenhum artefato visual dimensione o navegador do lado do cliente. </p> <p>Clique no URL para abrir a página da Web, redimensione a janela do navegador para acessar pontos de interrupção de layout diferentes e monitorar o tráfego da rede. </p> <p>Os casos de uso mais avançados incluem a associação de diferentes Predefinições de imagem ou comandos de Exibição de imagem, ou ambos, com valores de ponto de interrupção diferentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>Neste próximo exemplo, são usadas Predefinições de imagem de diferentes tamanhos de ponto de interrupção. Para um pequeno ponto de interrupção, uma predefinição de baixa qualidade é aplicada, o que força o Serviço de imagem a retornar a imagem GIF compactada apenas para seis cores. Um ponto de interrupção médio está usando uma Predefinição de imagem configurada para JPEG com alta compactação. O maior ponto de interrupção está associado a uma Predefinição de imagem de alta qualidade usando PNG sem perdas. Esse método garante que imagens de alta qualidade sejam fornecidas a esses dispositivos, com base no pressuposto de que os dispositivos com telas maiores têm maior largura de banda e poder de processamento. </p> <p>Clique no URL para abrir a página da Web, redimensione a janela do navegador da Web de maior para menor e observe como a qualidade da imagem degrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>Além das Predefinições de imagem, é possível associar comandos específicos do Image Serving a pontos de interrupção. O exemplo a seguir mostra como é possível cortar gradualmente a imagem do banner para a região de interesse, à medida que o tamanho da imagem na tela se torna menor. Aqui, o maior ponto de interrupção não tem nenhum comando Image Serving, então a imagem do banner é totalmente visível. No ponto de interrupção médio aplica recorte moderado, tornando visível somente o cursor com texto "Em execução". Em um ponto de interrupção pequeno, mais corte é aplicado para que somente o produto seja exibido. </p> <p>Clique no URL para abrir a página da Web e redimensionar a janela do navegador. Observe como a imagem se recorta gradualmente à medida que você vai de um tamanho maior para um menor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>Também é possível usar comandos de Exibição de imagem com Modelos de Exibição de imagem para controlar determinados parâmetros de modelo com base no tamanho da imagem. Neste próximo exemplo, um Modelo de disponibilização de imagens é usado em que o tamanho da fonte da sobreposição de texto é parametrizado usando o parâmetro <span class="codeph"> $fontsize </span>. A imagem responsiva é configurada para usar um tamanho de fonte maior para tamanhos de imagem menores, para garantir que o texto sempre permaneça legível: </p> </td> 
  </tr> 
 </tbody> 
</table>

## Requisitos do sistema {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**Hardware e software para servidor**

* Dynamic Media Image Serving 6.0.1 ou posterior.

**Requisitos mínimos do navegador do cliente**

* Microsoft® Windows® 7 ou posterior; Mac OS X 10.8 ou posterior.
* Firefox 23, Safari 6, Chrome 29, IE 9 ou posterior.
* iOS 6 ou posterior.
* Certificado no iPhone3GS ou posterior e no iPad2 ou posterior (somente navegadores nativos).
* Android OS 2.3 ou posterior.
* O Internet Explorer em dispositivos móveis não é compatível no momento.

