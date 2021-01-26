---
description: Atualiza as configurações de formato de publicação de vinheta.
seo-description: Atualiza as configurações de formato de publicação de vinheta.
seo-title: updateVignettePublishFormat
solution: Experience Manager
title: updateVignettePublishFormat
topic: Dynamic Media Image Production System API
uuid: ef8ae609-56e8-4ed6-906b-0668c5873946
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---


# updateVignettePublishFormat{#updatevignettepublishformat}

Atualiza as configurações de formato de publicação de vinheta.

## Tipos de usuário autorizados {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-8c7ba8d2bce14071b21fccb11f44749f}

**Entrada (updateVignettePublishFormatParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | Alça da empresa. |
| `*`vignetteFormatHandle`*` | `xsd:string` | Sim | Identificador de formato de publicação. |
| `*`name`*` | `xsd:string` | Não | Nome do formato de publicação. |
| `*`targetWidth`*` | `xsd:int` | Sim | Especifica a largura do público alvo da visualização de vinheta resultante em pixels. Use zero para que a vinheta de saída tenha o mesmo tamanho que a vinheta primária. |
| `*`targetHeight`*` | `xsd:int` | Sim | Especifica a altura do público alvo da visualização de vinheta resultante em pixels. Use zero para que a vinheta de saída tenha o mesmo tamanho que a vinheta primária. |
| `*`createPirâmid`*` | `xsd:boolean` | Sim | Cria uma vinheta pirâmide otimizada para aumentar o zoom no servidor de renderização de imagem. A partir do tamanho máximo, definido pelos campos Tamanho da vinheta do Público alvo, isso cria visualizações de vários tamanhos em um único arquivo de saída de vinheta. Cada tamanho de visualização subsequente é dividido em metade até que a largura e a altura estejam dentro de 128x128 pixels. |
| `*`thumbWidth`*` | `xsd:int` | Sim | Especifica a largura de cada miniatura resultante em pixels. Esta configuração é opcional. Deixe como zero para nenhum arquivo de miniatura. |
| `*`saveAsVersion`*` | `xsd:int` | Sim | Especifica o formato de arquivo para as vinhetas publicadas. Dada uma nova versão da Criação de imagens e uma versão mais antiga do Servidor de renderização de imagens, você deve especificar uma versão de vinheta que o Servidor de renderização de imagens pode ler. Se você especificar uma versão superior, o servidor de renderização de imagem não poderá ler as vinhetas publicadas. Defina como zero para publicar vinhetas na versão mais recente. |
| `*`sizeSuffixSeparator`*` | `xsd:string` | Sim | Especifica o caractere que separa o nome da vinheta e o sufixo que indica sua largura. |
| `*`afiador`*` | `xsd:int` | Não | Aplica a nitidez à imagem de visualização principal para cada tamanho de vinheta de publicação. A nitidez pode compensar a desfocagem quando as vinhetas são dimensionadas. |
| `*`usmAmount`*` | `xsd:double` | Sim | O mascaramento de nitidez digital é uma maneira flexível e poderosa de aumentar a nitidez, especialmente em imagens digitalizadas. Isso controla a magnitude de cada overshot (quanto mais escuras e mais claras as bordas se tornam). |
| `*`usmRadius`*` | `xsd:double` | Sim | Afeta o tamanho das bordas a serem melhoradas ou a largura das bordas, de modo que um raio menor melhora os detalhes em escala menor. Valores de raio mais altos podem causar halos nas bordas. O detalhe fino precisa de um raio menor, pois pequenos detalhes do mesmo tamanho ou menores que o raio são perdidos. |
| `*`usmThreshold`*` | `xsd:int` | Sim | Controla a alteração mínima de brilho para ser afiada ou a distância que deve estar entre os valores de tons adjacentes antes que o filtro funcione. Essa configuração pode tornar mais nítidas as bordas mais pronunciadas, deixando as bordas mais sutis intocadas. O intervalo permitido de limite é de 0 a 255. |

**Saída (updateVignettePublishFormatReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`vignetteFormatHandle`*` | `xsd:string` | Sim | Manuseie o formato de publicação de vinheta atualizado. |

## Exemplo {#section-fcba4bf2b7264786a676e315a35dbe43}

Este exemplo de código atualiza um formato de publicação de vinheta e retorna o identificador para o formato atualizado.

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

