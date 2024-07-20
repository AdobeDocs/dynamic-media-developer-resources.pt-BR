---
description: Atualiza as configurações de formato de publicação da vinheta.
solution: Experience Manager
title: updateVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7f199ed4-375f-4451-b66a-e50bcd55bf23
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---

# updateVignettePublishFormat{#updatevignettepublishformat}

Atualiza as configurações de formato de publicação da vinheta.

## Tipos de usuário autorizados {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-8c7ba8d2bce14071b21fccb11f44749f}

**Entrada (updateVignettePublishFormatParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | Identificador da empresa. |
| vinhetaFormatarAlça | `xsd:string` | Sim | Identificador de formato do Publish. |
| name | `xsd:string` | Não | Nome do formato Publish. |
| targetWidth | `xsd:int` | Sim | Especifica a largura alvo da exibição de vinheta resultante em pixels. Use zero para que a vinheta de saída tenha o mesmo tamanho da vinheta principal. |
| targetHeight | `xsd:int` | Sim | Especifica a altura de destino da exibição de vinheta resultante em pixels. Use zero para que a vinheta de saída tenha o mesmo tamanho da vinheta principal. |
| createPyramid | `xsd:boolean` | Sim | Cria uma vinheta em pirâmide otimizada para aplicar zoom no servidor de Renderização de imagem. Começando pelo tamanho máximo, definido pelos campos Tamanho da vinheta do Target, isso cria várias exibições de tamanho em um único arquivo de saída de vinheta. Cada tamanho de exibição subsequente é reduzido pela metade até que a largura e a altura fiquem dentro de 128x128 pixels. |
| thumbWidth | `xsd:int` | Sim | Especifica a largura de cada miniatura resultante em pixels. Esta configuração é opcional. Deixe como zero para nenhum arquivo de miniatura. |
| saveAsVersion | `xsd:int` | Sim | Especifica o formato de arquivo para as vinhetas publicadas. Dada uma nova versão da Criação de imagem e uma versão mais antiga do Servidor de renderização de imagem, você deve especificar uma versão de vinheta que seu Servidor de renderização de imagem possa ler. Se você especificar uma versão superior, o servidor de Renderização de Imagem não poderá ler as vinhetas publicadas. Defina como zero para publicar vinhetas na versão mais recente. |
| sizeSuffixSeparator | `xsd:string` | Sim | Especifica o caractere que separa o nome da vinheta e o sufixo que indica sua largura. |
| nitidez | `xsd:int` | Não | Aplica nitidez à imagem de exibição principal para cada tamanho de vinheta de publicação. A nitidez pode compensar o desfoque quando as vinhetas são dimensionadas. |
| usmAmount | `xsd:double` | Sim | O mascaramento digital sem nitidez é uma maneira flexível e eficiente de aumentar a nitidez, especialmente em imagens digitalizadas. Isso controla a magnitude de cada superação (o quanto mais escuro e mais claro as bordas se tornam). |
| usmRadius | `xsd:double` | Sim | Afeta o tamanho das bordas a serem aprimoradas ou a largura das bordas, portanto, um raio menor melhora os detalhes de escala menor. Valores de raio mais altos podem causar halos nas bordas. Detalhes finos precisam de um raio menor, pois detalhes pequenos do mesmo tamanho ou menores do que o raio são perdidos. |
| usmThreshold | `xsd:int` | Sim | Controla a alteração mínima de brilho a ser nitidez ou a distância entre os valores de tons adjacentes antes do funcionamento do filtro. Essa configuração pode ajustar a nitidez de bordas mais pronunciadas, deixando bordas mais sutis intocadas. O intervalo de limite permitido é de 0 a 255. |

**Saída (updateVignettePublishFormatReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| vinhetaFormatarAlça | `xsd:string` | Sim | Processe o formato de publicação de vinheta atualizado. |

## Exemplo {#section-fcba4bf2b7264786a676e315a35dbe43}

Este exemplo de código atualiza um formato de publicação de vinheta e retorna o identificador ao formato atualizado.

**Solicitação**

```java
<updateVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
   <name>APIcreateVignettePublishFormat2</name>
   <targetWidth>1000</targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>false</createPyramid>
   <thumbWidth>100</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>240.0</usmAmount>
   <usmRadius>3.1</usmRadius>
   <usmThreshold>150</usmThreshold>
</updateVignettePublishFormatParam>
```

**Resposta**

```java
<updateVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
</updateVignettePublishFormatReturn>
```
