---
title: VisualizadorPanorâmico
description: Construtor, cria uma instância do Visualizador Panorâmico HTML5.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---

# VisualizadorPanorâmico{#panoramicviewer}

`PanoramicViewer([config])`
Construtor, cria uma instância do Visualizador Panorâmico HTML5.

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
