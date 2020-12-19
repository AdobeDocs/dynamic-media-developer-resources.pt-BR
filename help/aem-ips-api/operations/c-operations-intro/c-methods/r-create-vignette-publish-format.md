---
description: Cria um novo formato de publicação para uma vinheta.
seo-description: Cria um novo formato de publicação para uma vinheta.
seo-title: createVignettePublishFormat
solution: Experience Manager
title: createVignettePublishFormat
topic: Scene7 Image Production System API
uuid: 834ebe6a-e105-4075-8004-172237980933
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---


# createVignettePublishFormat{#createvignettepublishformat}

Cria um novo formato de publicação para uma vinheta.

Os formatos de vinheta especificam o tamanho das vinhetas publicadas e suas miniaturas, bem como os níveis de zoom, os parâmetros de nitidez e a versão do formato de arquivo para vinhetas produzidas a partir de vinhetas primárias publicadas em um servidor de renderização de imagem a partir do IPS.

As versões mais recentes do servidor de renderização de imagens podem oferecer suporte a vinhetas pirâmides, o que elimina a necessidade de definir tamanhos específicos de formato de vinheta para publicação.

## Tipos de usuário autorizados {#section-f5c563e3695c4dba8df41e2a965aace7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-3a368186ec1d4005bca056fc9d9bacc7}

**Entrada (createVignettePublishFormatParam)**

<table id="table_4D5B2913FA784EC09190F25223C1A680"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Obrigatório </th> 
   <th colname="col4" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Manuseie a empresa à qual a vinheta pertence. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Nome para identificar o formato de publicação de vinheta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> <p>Especifica a largura do público alvo da visualização de vinheta resultante em pixels. </p> <p>Use zero para que a vinheta de saída tenha o mesmo tamanho que a vinheta primária. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Cria uma vinheta pirâmide otimizada para aumentar o zoom no servidor de renderização de imagem. A partir do tamanho máximo, definido pelos campos Tamanho da vinheta do Público alvo, isso cria visualizações de vários tamanhos em um único arquivo de saída de vinheta. Cada tamanho de visualização subsequente é dividido em metade até que a largura e a altura estejam dentro de 128x128 pixels. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPirâmid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Especifica a largura de cada miniatura resultante em pixels. Esta configuração é opcional. Deixe como zero para nenhum arquivo de miniatura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Especifica o formato de arquivo para as vinhetas publicadas. Dada uma nova versão do Image Authoring e uma versão mais antiga do Image Rendering Server, você deve especificar uma versão de vinheta que o ImageRendering Server pode ler. Se você especificar uma versão superior, o servidor de renderização de imagem não poderá ler as vinhetas publicadas. Defina como zero para publicar vinhetas na versão mais recente. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Especifica o caractere que separa o nome da vinheta e o sufixo que indica sua largura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Especifica o caractere que separa o nome da vinheta e o sufixo que indica sua largura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> afiador</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Aplica a nitidez à imagem da visualização principal para cada tamanho de vinheta de publicação A nitidez pode compensar a indefinição quando os vinhetas são dimensionados. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> O mascaramento de nitidez digital é uma maneira flexível e poderosa de aumentar a nitidez, especialmente em imagens digitalizadas. Isso controla a magnitude de cada overshot (quanto mais escuras e claras as bordas se tornam). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Afeta o tamanho das bordas a serem melhoradas ou a largura das bordas, de modo que um raio menor melhora os detalhes em menor escala. Valores de raio mais altos podem causar halos nas bordas. O detalhe fino precisa de um raio menor, pois pequenos detalhes do mesmo tamanho ou menores que o raio são perdidos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase de código  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Controla a alteração mínima de brilho para ser afiada ou a distância que deve estar entre os valores de tons adjacentes antes que o filtro funcione. Essa configuração pode tornar mais nítidas as bordas mais pronunciadas, deixando as bordas mais sutis intocadas. O intervalo permitido de limite de 0 a 255. </td> 
  </tr> 
 </tbody> 
</table>

**Saída (createVignettePublishFormatReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| ` *`vignetteFormatHandle`*` | `xsd:string` | Sim | O identificador do formato de vinheta criado. |

## Exemplos {#section-0564752d439642b9bb8de2903db6de1e}

Esse código cria o formato de publicação de vinheta. A solicitação de criação especifica um nome, a largura e a altura do público alvo e outros valores obrigatórios.

**Solicitação**

```java
<createVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <name>APIcreateVignettePublishFormat1</name>
   <targetWidth>1200</<targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>true</createPyramid>
   <thumbWidth>400</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>230.0</usmAmount>
   <usmRadius>1.1</usmRadius>
   <usmThreshold>130</usmThreshold>
</createVignettePublishFormatParam>
```

**Resposta**

```java
<createVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</createVignettePublishFormatReturn>
```

