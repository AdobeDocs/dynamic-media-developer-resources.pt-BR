---
description: Os atributos de configuração são definidos como atributos diretamente em um elemento IMG gerenciado pela biblioteca de imagens responsivas. Cada imagem pode ter seu próprio conjunto de atributos.
solution: Experience Manager
title: Referência de comando - Atributos de configuração
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8cc645f8-03fe-4ac7-b23f-36536b60fdf6
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Os atributos de configuração são definidos como atributos diretamente em um elemento IMG gerenciado pela biblioteca de imagens responsivas. Cada imagem pode ter seu próprio conjunto de atributos.

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

Opcional.

URL da imagem fornecida pelo Servidor de imagens. Se a URL não estiver presente, a biblioteca usará o valor definido no atributo `src` como fallback. Esse atributo serve a imagem inicial e a imagem dinâmica que a biblioteca de imagens responsivas gerencia de locais diferentes.

**Exemplo**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

Se `data-src` estiver definido, `src` será opcional e poderá conter qualquer URL que você queira adicionar. Por exemplo, ela pode conter um URL para a mesma imagem baseada no Servidor de imagens que a biblioteca usa. Ou pode conter um espaço reservado para GIF ou até mesmo um URI de dados para evitar uma viagem de ida e volta extra do servidor na inicialização.

Se `data-src` não estiver definido, `src` será obrigatório e deverá conter uma URL para a imagem fornecida pelo Servidor de imagens.

**Exemplo**

Usando URI de dados para o atributo `src` e URL do Servidor de imagens para o atributo `data-src`:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## pontos de interrupção de dados {#section-3bf62a89ff3e40569848c1fe3ac7886c}

Uma lista separada por vírgulas de pontos de interrupção e, opcionalmente, seguida por dois pontos ( `:`) e comandos do Servidor de imagens ou Predefinições de imagens. Cada ponto de interrupção é um valor de largura de imagem definido em pixels CSS lógicos. A biblioteca carrega a imagem com o valor maior mais próximo da lista e faz o downscale-la no cliente para corresponder à largura da imagem CSS de tempo de execução. (Se você trabalhar em uma tela de alta densidade, as representações de imagem carregadas do servidor representarão valores de pontos de interrupção multiplicados pela proporção de pixels do dispositivo).

Para qualquer ponto de interrupção da lista, é possível definir um ou mais comandos do Servidor de imagens ou nomes de Predefinições de imagens. Esses parâmetros extras são aplicados apenas à imagem caso esse ponto de interrupção específico esteja ativo no momento.

Você pode usar qualquer comando com suporte no Servidor de Imagens, exceto os comandos de exibição que afetam o tamanho da imagem de resposta, como `wid=`, `hei=` ou `scl=`. A mesma restrição se aplica às Predefinições de imagem: uma Predefinição de imagem usada com a Biblioteca de imagens responsiva não deve conter esses comandos.

Vários comandos do Servidor de imagens ou nomes de Predefinições de imagens são separados com o caractere &quot; `&`&quot;. Se um comando do Servidor de imagens tiver uma vírgula em seu valor, essa vírgula será substituída por `%2C`. Os nomes das Predefinições de imagem são colocados em cifrões ( `$`).

**Exemplos**

**Usando somente pontos de interrupção**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**Usando comandos do Servidor de Imagens**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**Usando predefinições de imagem**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**Usando predefinições de imagem e comandos do Servidor de imagens**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## modo de dados {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

Os dois modos de Corte inteligente a seguir estão disponíveis no AEM 6.4 e superior e nos Visualizadores do Dynamic Media 5.9 e superiores:

* **Manual** - os pontos de interrupção definidos pelo usuário e os comandos de Serviço de Imagem correspondentes são definidos em um atributo no elemento de imagem.
* **Recorte inteligente** - as representações de recorte inteligente computadas são recuperadas automaticamente do servidor de entrega. A melhor representação é selecionada usando o tamanho do tempo de execução do elemento de imagem.

Para usar o modo Corte inteligente, você define o atributo `data-mode` como `smart crop`.

**Exemplo**

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

O elemento de imagem associado despacha um evento `s7responsiveViewer` durante o tempo de execução quando o ponto de interrupção é alterado.

```html {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
