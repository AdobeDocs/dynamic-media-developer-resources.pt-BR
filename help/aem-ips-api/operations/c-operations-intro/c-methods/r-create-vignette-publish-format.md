---
description: Cria um novo formato de publicação para uma vinheta.
solution: Experience Manager
title: createVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d58e1290-8a79-4129-99ce-776b919dea13
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# createVignettePublishFormat{#createvignettepublishformat}

Cria um novo formato de publicação para uma vinheta.

Os formatos de vinheta especificam o tamanho das vinhetas publicadas e suas miniaturas, bem como os níveis de zoom, os parâmetros de nitidez e a versão do formato de arquivo das vinhetas produzidas a partir de vinhetas primárias publicadas em um servidor de Renderização de Imagem a partir de IPS.

As versões mais recentes do servidor de Renderização de imagem podem oferecer suporte a vinhetas em pirâmide, o que elimina a necessidade de definir tamanhos de formato de vinheta específicos para publicação.

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
   <td colname="col4"> Processe a empresa à qual a vinheta pertence. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nome</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase codificada </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Nome para identificar o formato de publicação da vinheta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase codificada </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> <p>Especifica a largura alvo da exibição de vinheta resultante em pixels. </p> <p>Use zero para que a vinheta de saída tenha o mesmo tamanho da vinheta principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase codificada </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Cria uma vinheta em pirâmide otimizada para aplicar zoom no servidor de Renderização de imagem. Começando pelo tamanho máximo, definido pelos campos Tamanho da vinheta do Target, isso cria várias exibições de tamanho em um único arquivo de saída de vinheta. Cada tamanho de exibição subsequente é reduzido pela metade até que a largura e a altura fiquem dentro de 128x128 pixels. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase codificada </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Especifica a largura de cada miniatura resultante em pixels. Esta configuração é opcional. Deixe como zero para nenhum arquivo de miniatura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase codificada </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Especifica o formato de arquivo para as vinhetas publicadas. Dada uma nova versão da Criação de imagem e uma versão anterior do Servidor de renderização de imagem, você deve especificar uma versão de vinheta que seu Servidor de renderização de imagem possa ler. Se você especificar uma versão superior, o servidor de Renderização de Imagem não poderá ler as vinhetas publicadas. Defina como zero para publicar vinhetas na versão mais recente. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase codificada </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Especifica o caractere que separa o nome da vinheta e o sufixo que indica sua largura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase codificada </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Especifica o caractere que separa o nome da vinheta e o sufixo que indica sua largura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nitidez</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase codificada </span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Aplica nitidez à imagem de exibição principal para cada tamanho de vinheta de publicação. A nitidez pode compensar o desfoque quando os vinhetas são dimensionados. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase codificada </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> O mascaramento digital sem nitidez é uma maneira flexível e eficiente de aumentar a nitidez, especialmente em imagens digitalizadas. Isso controla a magnitude de cada superação (o quanto mais escuro e claro se tornam as bordas). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase codificada </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Afeta o tamanho das bordas a serem aprimoradas ou a largura das bordas, de modo que um rádio menor melhora os detalhes de escala menor. Valores de raio mais altos podem causar halos nas bordas. Detalhes finos precisam de um raio menor, pois detalhes pequenos do mesmo tamanho ou menores do que o raio são perdidos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase codificada </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Controla a alteração mínima de brilho a ser nitidez ou a distância entre os valores de tons adjacentes antes do funcionamento do filtro. Essa configuração pode ajustar a nitidez de bordas mais pronunciadas, deixando bordas mais sutis intocadas. O intervalo permitido de limite de 0 a 255. </td> 
  </tr> 
 </tbody> 
</table>

**Saída (createVignettePublishFormatReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| vinhetaFormatarAlça | `xsd:string` | Sim | O identificador para o formato de vinheta criado. |

## Exemplos {#section-0564752d439642b9bb8de2903db6de1e}

Esse código cria o formato de publicação de vinheta. A solicitação de criação especifica um nome, a largura e a altura do público-alvo e outros valores necessários.

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
