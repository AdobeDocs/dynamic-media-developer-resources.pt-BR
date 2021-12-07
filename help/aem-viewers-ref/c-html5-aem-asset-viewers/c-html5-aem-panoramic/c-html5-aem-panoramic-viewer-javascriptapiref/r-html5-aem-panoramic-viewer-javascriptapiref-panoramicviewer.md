---
title: PanorâmicaViewer
description: Construtor, cria uma nova instância HTML5 do Visualizador de carrossel.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# PanorâmicaViewer{#panoramicviewer}

`PanoramicViewer([config])`
Construtor, cria uma nova instância HTML5 Panorâmica Viewer.

## Parâmetro {#section-fa807db629ce43bab286b1e1dc96c492}

config {Object} objeto de configuração JSON opcional, permite passar todas as configurações do visualizador para o construtor e evitar chamar métodos de setter individuais. Contém as seguintes propriedades:
* containerId - {String} ID do contêiner DOM (normalmente um DIV) no qual o visualizador será inserido. Não é necessário ter o elemento de contêiner criado pelo momento em que esse método é chamado, no entanto, o contêiner deve existir quando init() é executado. Obrigatório
* params - objeto JSON {Object} com parâmetros de configuração do visualizador em que o nome da propriedade é a opção de configuração específica do visualizador ou o modificador do SDK, e o valor dessa propriedade é um valor de configurações correspondente. Obrigatório
* manipuladores - objeto JSON {Object} com retornos de chamada do evento do visualizador, em que o nome da propriedade é o nome do evento do visualizador suportado e o valor da propriedade é uma referência de função JavaScript para o retorno de chamada apropriado. Consulte a seção Retornos de chamada do evento para obter mais informações sobre os eventos do visualizador. Opcional


## Devoluções {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nenhum.

## Exemplo {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
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
