---
title: VisualizadorPanorâmico
description: ', cria uma instância do Visualizador panorâmico do HTML5.'
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
source-git-commit: 07380e01e4eed6a65ba8821eee3db6fd9bb19639
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# VisualizadorPanorâmico{#panoramicviewer}

`PanoramicViewer([config])`
, cria uma instância do Visualizador panorâmico do HTML5.

## Parâmetro {#section-fa807db629ce43bab286b1e1dc96c492}

config
O objeto de configuração JSON opcional {Object} permite passar todas as configurações do visualizador para o construtor e evitar a chamada de métodos setter individuais. Ele contém as seguintes propriedades:

* containerId - {String} ID do contêiner DOM (normalmente um DIV) no qual o visualizador é inserido. Não é necessário ter o elemento de contêiner criado no momento em que esse método é chamado, no entanto, o contêiner deve existir quando init() é executado. Obrigatório
* parâmetros - {Object} objeto JSON com parâmetros de configuração do visualizador em que o nome da propriedade é uma opção de configuração específica do visualizador ou um modificador SDK, e o valor dessa propriedade é um valor de configurações correspondente. Obrigatório
* manipuladores - {Object} objeto JSON com retornos de chamada do evento do visualizador, em que o nome da propriedade é o nome do evento do visualizador com suporte e o valor da propriedade é uma referência de função JavaScript para o retorno de chamada apropriado. Consulte a seção Retornos de chamada de evento para obter mais informações sobre eventos do visualizador. Opcional.


## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
    "serverurl":"http://s7d1.scene7.com/is/image/"
},
"handlers":{
    "initComplete":function() {
        console.log("init complete");
}
}
});
```
