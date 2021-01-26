---
description: Os atributos de configuração são definidos como atributos diretamente em um elemento IMG gerenciado pela biblioteca de Imagem responsiva. Cada imagem pode ter seu próprio conjunto de atributos.
seo-description: Os atributos de configuração são definidos como atributos diretamente em um elemento IMG gerenciado pela biblioteca de Imagem responsiva. Cada imagem pode ter seu próprio conjunto de atributos.
seo-title: Referência de comando - Atributos de configuração
solution: Experience Manager
title: Referência de comando - Atributos de configuração
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a3d52680-2a28-40c8-9b5f-b1c252c88e4d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 0%

---


# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Os atributos de configuração são definidos como atributos diretamente em um elemento IMG gerenciado pela biblioteca de Imagem responsiva. Cada imagem pode ter seu próprio conjunto de atributos.

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

Opcional.

URL da imagem que o Serviço de Imagens serve. Se o URL não estiver presente, a biblioteca usará o valor definido no atributo `src` como fallback. Esse atributo serve a imagem inicial e a imagem dinâmica que a biblioteca de Imagem responsiva gerencia de diferentes locais.

**Exemplo**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

Se `data-src` estiver definido, `src` é opcional e pode conter qualquer URL que você deseja adicionar. Por exemplo, pode conter um URL para a mesma imagem baseada no Servidor de imagens que a biblioteca usa. Ou pode conter um espaço reservado GIF ou até mesmo um URI de dados para evitar um percurso de ida e volta extra do servidor na inicialização.

Se `data-src` não estiver definido, `src` será obrigatório e deverá conter um URL para a imagem que o Serviço de Imagens serve.

**Exemplo**

Usando o URI de dados para o atributo `src` e o URL de disponibilização de imagem para o atributo `data-src`:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## pontos de interrupção de dados {#section-3bf62a89ff3e40569848c1fe3ac7886c}

Uma lista separada por vírgulas de pontos de interrupção e, opcionalmente, seguida por dois pontos ( `:`) e comandos de Servidor de imagens ou Predefinições de imagens. Cada ponto de interrupção é um valor de largura de imagem definido em pixels CSS lógicos. A biblioteca carrega a imagem com o valor maior mais próximo da lista e a baixa no cliente para corresponder à largura da imagem CSS do tempo de execução. (Se você trabalha em uma tela de alta densidade, as representações de imagem carregadas do servidor representam valores de ponto de interrupção multiplicados pela proporção de pixels do dispositivo).

Para qualquer ponto de interrupção da lista, é possível definir um ou mais comandos do Servidor de imagens ou nomes de predefinições de imagens. Esses parâmetros extras são aplicados apenas à imagem caso esse ponto de interrupção específico esteja ativo no momento.

Você pode usar qualquer comando compatível com o Serviço de imagem, exceto os comandos de visualização que afetam o tamanho da imagem de resposta, como `wid=`, `hei=` ou `scl=`. A mesma restrição se aplica às predefinições de imagem: uma predefinição de imagem usada com a Biblioteca de imagens responsivas não deve conter esses comandos.

Vários comandos do Servidor de imagens ou nomes de predefinições de imagens são separados pelo caractere &quot; `&`&quot;. Se um comando do Servidor de imagens tiver uma vírgula em seu valor, essa vírgula será substituída por `%2C`. Os nomes predefinidos de imagem são vinculados em cifras ( `$`).

**Exemplos**

**Uso somente de pontos de interrupção**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**Uso de comandos do Servidor de imagens**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**Uso de predefinições de imagens**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**Uso de predefinições de imagens e comandos de disponibilização de imagens**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## modo de dados {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

Os dois modos de Recorte inteligente estão disponíveis no AEM 6.4 e superior e no Dynamic Media Viewers 5.9 e superior:

* **Manual**  - os pontos de interrupção definidos pelo usuário e os comandos correspondentes do Serviço de imagem são definidos dentro de um atributo no elemento de imagem.
* **Recorte**  inteligente - execuções de recorte inteligente calculadas são recuperadas automaticamente do servidor de delivery. A melhor representação é selecionada usando o tamanho do tempo de execução do elemento de imagem.

Para usar o modo de Recorte inteligente, defina o atributo `data-mode` como `smart crop`.

**Exemplo**

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

O elemento de imagem associado despacha um evento `s7responsiveViewer` durante o tempo de execução quando o ponto de interrupção é alterado.

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```

