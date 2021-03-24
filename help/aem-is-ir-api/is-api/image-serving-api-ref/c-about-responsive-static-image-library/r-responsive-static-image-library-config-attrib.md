---
description: Os atributos de configuração são definidos como atributos diretamente em um elemento IMG que a biblioteca de Imagem responsiva gerencia. Cada imagem pode ter seu próprio conjunto de atributos.
solution: Experience Manager
title: Referência de comando - Atributos de configuração
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---


# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Os atributos de configuração são definidos como atributos diretamente em um elemento IMG que a biblioteca de Imagem responsiva gerencia. Cada imagem pode ter seu próprio conjunto de atributos.

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

Opcional.

URL da imagem que a Exibição de imagem serve. Se o URL não estiver presente, a biblioteca usará o valor definido no atributo `src` como fallback. Esse atributo fornece a imagem inicial e a dinâmica que a biblioteca de Imagem responsiva gerencia de diferentes locais.

**Exemplo**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

Se `data-src` for definido, `src` será opcional e poderá conter qualquer URL que deseja adicionar. Por exemplo, ele pode conter um URL para a mesma imagem baseada no fornecimento de imagem que a biblioteca usa. Ou pode conter um espaço reservado GIF ou até mesmo um URI de dados para evitar um caminho de ida e volta extra do servidor na inicialização.

Se `data-src` não estiver definido, `src` é obrigatório e deve conter um URL para a imagem que o Image Serving serve.

**Exemplo**

Usando o URI de dados para o atributo `src` e o URL de Exibição de Imagem para o atributo `data-src`:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## pontos de interrupção de dados {#section-3bf62a89ff3e40569848c1fe3ac7886c}

Uma lista separada por vírgulas de pontos de interrupção e opcionalmente seguida por dois pontos ( `:`) e comandos de Exibição de imagem ou Predefinições de imagem. Cada ponto de interrupção é um valor de largura de imagem definido em pixels CSS lógicos. A biblioteca carrega a imagem com o valor maior mais próximo da lista e a baixa no cliente para corresponder à largura da imagem CSS do tempo de execução. (Se você trabalha em uma tela de alta densidade, as representações de imagem carregadas do servidor representam valores de ponto de interrupção multiplicados pela proporção de pixels do dispositivo).

Para qualquer ponto de interrupção da lista, é possível definir um ou mais comandos do Image Serving ou nomes de predefinições de imagens. Esses parâmetros extras são aplicados apenas à imagem caso esse ponto de interrupção específico esteja ativo no momento.

Você pode usar qualquer comando de Exibição de imagem compatível, exceto para os comandos de exibição que afetam o tamanho da imagem de resposta, como `wid=`, `hei=` ou `scl=`. A mesma restrição se aplica às Predefinições de imagem: uma Predefinição de imagem usada com a Biblioteca de imagens responsivas não deve conter esses comandos.

Vários comandos do Image Serving ou nomes de predefinições de imagens são separados por um caractere &quot; `&`&quot;. Se um comando Image Serving tiver uma vírgula em seu valor, essa vírgula será substituída por `%2C`. Os nomes de predefinições da imagem são envolvidos em cifrões ( `$`).

**Exemplos**

**Uso somente de pontos de interrupção**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**Uso de comandos do Image Serving**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**Uso de predefinições de imagem**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**Uso de predefinições de imagens e comandos de disponibilização de imagens**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## modo de dados {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

Os dois modos de Recorte inteligente a seguir estão disponíveis no AEM 6.4 e superior e no Dynamic Media Viewers 5.9 e superior:

* **Manual**  - os pontos de interrupção definidos pelo usuário e os comandos correspondentes do Serviço de imagem são definidos em um atributo no elemento de imagem.
* **Recorte inteligente**  - as representações de recorte inteligente calculadas são recuperadas automaticamente do servidor de delivery. A melhor representação é selecionada usando o tamanho do tempo de execução do elemento de imagem.

Para usar o modo Recorte inteligente, defina o atributo `data-mode` para `smart crop`.

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

