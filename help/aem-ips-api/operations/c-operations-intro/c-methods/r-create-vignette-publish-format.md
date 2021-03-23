---
description: Cria um novo formato de publicação para uma vinheta.
seo-description: Cria um novo formato de publicação para uma vinheta.
seo-title: createVignettePublishFormat
solution: Experience Manager
title: createVignettePublishFormat
uuid: 834ebe6a-e105-4075-8004-172237980933
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 0%

---


# createVignettePublishFormat{#createvignettepublishformat}

Cria um novo formato de publicação para uma vinheta.

Os formatos de vinheta especificam o tamanho das vinhetas publicadas e suas miniaturas, bem como os níveis de zoom, os parâmetros de nitidez e a versão do formato de arquivo para vinhetas produzidas a partir de vinhetas primárias publicadas em um servidor de Renderização de imagem do IPS.

As versões mais recentes do servidor de Renderização de imagem podem oferecer suporte a vinhetas pirâmides, o que elimina a necessidade de definir tamanhos específicos de formato de vinheta para publicação.

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
   <td colname="col4"> Lide com a empresa à qual a vinheta pertence. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase do código  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Nome para identificar o formato de publicação da vinheta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase do código  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> <p>Especifica a largura de destino da exibição de vinheta resultante em pixels. </p> <p>Use zero para que a vinheta de saída tenha o mesmo tamanho da vinheta primária. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase do código  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Cria uma vinheta pirâmide otimizada para aumentar o zoom no servidor de Renderização de imagem. Começando pelo tamanho máximo, definido pelos campos Tamanho da vinheta do Target, isso cria visualizações de vários tamanhos em um único arquivo de saída da vinheta. Cada tamanho de exibição subsequente é dividido até que a largura e a altura estejam dentro de 128x128 pixels. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase do código  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Especifica a largura de cada miniatura resultante em pixels. Essa configuração é opcional. Deixe como zero para nenhum arquivo de miniatura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase do código  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Especifica o formato de arquivo para as vinhetas publicadas. Dada uma nova versão da Criação de Imagens e uma versão mais antiga do Servidor de Renderização de Imagens, você deve especificar uma versão de vinheta que seu Servidor de Renderização de Imagens possa ler. Se você especificar uma versão superior, o servidor de Renderização de imagem não poderá ler as vinhetas publicadas. Defina como zero para publicar vinhetas na versão mais recente. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase do código  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Especifica o caractere que separa o nome da vinheta e o sufixo que indica sua largura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase do código  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Especifica o caractere que separa o nome da vinheta e o sufixo que indica sua largura. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> afiador</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase do código  </span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Aplica nitidez à imagem de exibição principal para cada vinheta de publicação A nitidez pode compensar o desfoque quando as vinhetas são dimensionadas. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase do código  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> O mascaramento com nitidez digital é uma maneira flexível e poderosa de aumentar a nitidez, especialmente em imagens digitalizadas. Isso controla a magnitude de cada superação (quanto mais escuro e claro as bordas se tornam). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase do código  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Afeta o tamanho das bordas a serem melhoradas ou a largura das bordas, de modo que um raio menor melhora detalhes em escala menor. Valores de raio mais altos podem causar halos nas bordas. Os detalhes finos precisam de um raio menor, pois detalhes minúsculos do mesmo tamanho ou menores que o raio é perdido. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Frase do código  </span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Controla a alteração mínima do brilho para ser nitidamente definida ou a distância que os valores de tons adjacentes devem estar entre si antes que o filtro funcione. Essa configuração pode tornar as bordas mais pronunciadas mais nítidas, deixando as bordas mais sutis intocadas. O intervalo permitido de 0 a 255. </td> 
  </tr> 
 </tbody> 
</table>

**Saída (createVignettePublishFormatReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`vinhetaFormatarIdentificador`*` | `xsd:string` | Sim | O identificador para o formato de vinheta criado. |

## Exemplos {#section-0564752d439642b9bb8de2903db6de1e}

Esse código cria o formato de publicação da vinheta. A solicitação de criação especifica um nome, a largura e a altura do target e outros valores necessários.

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

