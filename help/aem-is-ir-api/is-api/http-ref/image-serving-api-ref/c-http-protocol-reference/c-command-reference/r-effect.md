---
description: Selecione Camada de efeito. Seleciona uma camada de efeito e inicia um novo segmento de camada na cadeia de caracteres de solicitação, que está associada à camada atual.
seo-description: Selecione Camada de efeito. Seleciona uma camada de efeito e inicia um novo segmento de camada na cadeia de caracteres de solicitação, que está associada à camada atual.
seo-title: efeito
solution: Experience Manager
title: efeito
uuid: 622dc7ca-55b8-4a82-b9a7-65588aee87d0
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---


# efeito{#effect}

Selecione Camada de efeito. Seleciona uma camada de efeito e inicia um novo segmento de camada na cadeia de caracteres de solicitação, que está associada à camada atual.

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>Número da camada do efeito (não é igual a 0). </p></td> 
 </tr> 
</table>

Todos os comandos no novo segmento são aplicados à camada de efeito especificada. Um segmento de camada de efeito é encerrado pelo próximo comando `layer=` ou `effect=` ou pelo final da solicitação.

*`n`* deve ser inferior a 0 para efeitos da camada exterior (ou seja, efeitos por trás da camada principal) e superior a 0 para efeitos da camada interna (ou seja, efeitos dentro da camada principal). Os números de camada de efeito não precisam ser consecutivos.

O número da camada de efeito especifica a ordem z, no caso de várias camadas de efeito para a mesma camada pai. As camadas com número mais alto são colocadas sobre as camadas com número mais baixo.

As camadas de efeito podem ser anexadas a `layer=comp`.

## Propriedades {#section-e11f795deff345779ce280a82cf221ca}

Comando da camada de efeito. *`n`* não deve ser 0.

## Padrão {#section-84bbe1cfe7a94040827c994323ac59d4}

Nenhum.

## Exemplo {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## Consulte também {#section-573273e9e0e64103a5764075f5e50180}

` [layer=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md#reference-0f8d7fbef64841dd855917bd8fc22e6d)`
