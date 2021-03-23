---
description: Atualiza as configurações de formato de publicação da vinheta.
seo-description: Atualiza as configurações de formato de publicação da vinheta.
seo-title: updateVignettePublishFormat
solution: Experience Manager
title: updateVignettePublishFormat
uuid: ef8ae609-56e8-4ed6-906b-0668c5873946
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '448'
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
| `*`companyHandle`*` | `xsd:string` | Sim | Manuseio da empresa. |
| `*`vinhetaFormatarIdentificador`*` | `xsd:string` | Sim | Publicar identificador de formato. |
| `*`name`*` | `xsd:string` | Não | Nome do formato de publicação. |
| `*`targetWidth`*` | `xsd:int` | Sim | Especifica a largura de destino da exibição de vinheta resultante em pixels. Use zero para que a vinheta de saída tenha o mesmo tamanho da vinheta primária. |
| `*`targetHeight`*` | `xsd:int` | Sim | Especifica a altura do target da exibição de vinheta resultante em pixels. Use zero para que a vinheta de saída tenha o mesmo tamanho da vinheta primária. |
| `*`createPyramid`*` | `xsd:boolean` | Sim | Cria uma vinheta pirâmide otimizada para aumentar o zoom no servidor de Renderização de imagem. Começando pelo tamanho máximo, definido pelos campos Tamanho da vinheta do Target, isso cria visualizações de vários tamanhos em um único arquivo de saída da vinheta. Cada tamanho de exibição subsequente é dividido até que a largura e a altura estejam dentro de 128x128 pixels. |
| `*`thumbWidth`*` | `xsd:int` | Sim | Especifica a largura de cada miniatura resultante em pixels. Essa configuração é opcional. Deixe como zero para nenhum arquivo de miniatura. |
| `*`saveAsVersion`*` | `xsd:int` | Sim | Especifica o formato de arquivo para as vinhetas publicadas. Dada uma nova versão da Criação de Imagens e uma versão mais antiga do Servidor de Renderização de Imagens, você deve especificar uma versão de vinheta que seu Servidor de Renderização de Imagens pode ler. Se você especificar uma versão superior, o servidor de Renderização de imagem não poderá ler as vinhetas publicadas. Defina como zero para publicar vinhetas na versão mais recente. |
| `*`sizeSuffixSeparator`*` | `xsd:string` | Sim | Especifica o caractere que separa o nome da vinheta e o sufixo que indica sua largura. |
| `*`afiador`*` | `xsd:int` | Não | Aplica nitidez à imagem de exibição principal para cada tamanho de vinheta de publicação. A nitidez pode compensar o desfoque quando as vinhetas são dimensionadas. |
| `*`usmAmount`*` | `xsd:double` | Sim | O mascaramento com nitidez digital é uma maneira flexível e poderosa de aumentar a nitidez, especialmente em imagens digitalizadas. Isso controla a magnitude de cada superação (quanto mais escuras e mais claras as bordas se tornam). |
| `*`usmRadius`*` | `xsd:double` | Sim | Afeta o tamanho das bordas a serem melhoradas ou a largura das bordas, de modo que um raio menor melhora detalhes em escala menor. Valores de raio mais altos podem causar halos nas bordas. Os detalhes finos precisam de um raio menor, pois detalhes minúsculos do mesmo tamanho ou menores que o raio é perdido. |
| `*`usmThreshold`*` | `xsd:int` | Sim | Controla a alteração mínima do brilho para ser nitidamente definida ou a distância que os valores de tons adjacentes devem estar entre si antes que o filtro funcione. Essa configuração pode tornar as bordas mais pronunciadas mais nítidas, deixando as bordas mais sutis intocadas. O intervalo permitido de limite é de 0 a 255. |

**Saída (updateVignettePublishFormatReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`vinhetaFormatarIdentificador`*` | `xsd:string` | Sim | Manipule o formato de publicação da vinheta atualizado. |

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

