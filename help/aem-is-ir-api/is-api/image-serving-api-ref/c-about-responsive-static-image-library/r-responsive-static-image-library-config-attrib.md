---
description: Os atributos de configuração são definidos como atributos diretamente em um elemento IMG gerenciado pela biblioteca de imagens responsivas. Cada imagem pode ter seu próprio conjunto de atributos.
solution: Experience Manager
title: Referência de comando - Atributos de configuração
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8cc645f8-03fe-4ac7-b23f-36536b60fdf6
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 0%

---

# Referência de comando - Atributos de configuração{#command-reference-configuration-attributes}

Os atributos de configuração são definidos como atributos diretamente em um elemento IMG gerenciado pela biblioteca de imagens responsivas. Cada imagem pode ter seu próprio conjunto de atributos.

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

Opcional.

URL da imagem fornecida pelo Servidor de imagens. Se o URL não estiver presente, a biblioteca usará o valor definido em `src` atributo como fallback. Esse atributo serve a imagem inicial e a imagem dinâmica que a biblioteca de imagens responsivas gerencia de locais diferentes.

**Exemplo**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

Se `data-src` está definido, `src` é opcional e pode conter qualquer URL que você deseja adicionar. Por exemplo, ela pode conter um URL para a mesma imagem baseada no Servidor de imagens que a biblioteca usa. Ou pode conter um espaço reservado para GIF ou até mesmo um URI de dados para evitar uma viagem de ida e volta extra do servidor na inicialização.

Se `data-src` não está definido, `src` é obrigatório e deve conter um URL para a imagem fornecida pelo Servidor de imagens.

**Exemplo**

Uso do URI de dados para o `src` Atributo e URL do Servidor de imagens para a `data-src` atributo:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## pontos de interrupção de dados {#section-3bf62a89ff3e40569848c1fe3ac7886c}

Uma lista separada por vírgulas de pontos de interrupção seguida, opcionalmente, por dois pontos ( `:`) e comandos do Servidor de imagens ou Predefinições de imagem. Cada ponto de interrupção é um valor de largura de imagem definido em pixels CSS lógicos. A biblioteca carrega a imagem com o valor maior mais próximo da lista e faz o downscale-la no cliente para corresponder à largura da imagem CSS de tempo de execução. (Se você trabalhar em uma tela de alta densidade, as representações de imagem carregadas do servidor representarão valores de pontos de interrupção multiplicados pela proporção de pixels do dispositivo).

Para qualquer ponto de interrupção da lista, é possível definir um ou mais comandos do Servidor de imagens ou nomes de Predefinições de imagens. Esses parâmetros extras são aplicados apenas à imagem caso esse ponto de interrupção específico esteja ativo no momento.

Você pode usar qualquer comando suportado do Servidor de imagens, exceto os comandos de visualização que afetam o tamanho da imagem de resposta, como `wid=`, `hei=`ou `scl=`. A mesma restrição se aplica às Predefinições de imagem: uma Predefinição de imagem usada com a Biblioteca de imagens responsiva não deve conter esses comandos.

Vários comandos do Servidor de imagens ou nomes de Predefinições de imagens são separados por &quot; `&`&quot;. Se um comando do Servidor de imagens tiver uma vírgula em seu valor, essa vírgula será substituída por `%2C`. Os nomes das predefinições de imagem são colocados em cifrões ( `$`).

**Exemplos**

**Usar somente pontos de interrupção**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**Uso de comandos do Servidor de imagens**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**Uso de predefinições de imagem**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**Uso de predefinições de imagem e comandos do Servidor de imagens**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## modo de dados {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

Os dois modos de Corte inteligente a seguir estão disponíveis no AEM 6.4 e superior e no Dynamic Media Viewers 5.9 e superior:

* **Manual** - pontos de interrupção definidos pelo usuário e comandos correspondentes do Serviço de imagens são definidos em um atributo no elemento de imagem.
* **Corte inteligente** - as representações de corte inteligente calculadas são recuperadas automaticamente do servidor de entrega. A melhor representação é selecionada usando o tamanho do tempo de execução do elemento de imagem.

Para usar o modo Corte inteligente, defina a `data-mode` atributo para `smart crop`.

**Exemplo**

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

O elemento de imagem associado envia um `s7responsiveViewer` durante o tempo de execução quando o ponto de interrupção muda.

```html {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
