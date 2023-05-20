---
title: efeito
description: Selecione Camada de efeito. Seleciona uma camada de efeito e inicia um novo segmento de camada na cadeia de caracteres de solicitação, que está associada à camada atual.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1eaa38d-cfd3-44d4-92b1-04d72333f867
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---

# efeito{#effect}

Selecione Camada de efeito. Seleciona uma camada de efeito e inicia um novo segmento de camada na cadeia de caracteres de solicitação, que está associada à camada atual.

`effect= *`n`*`

<table id="simpletable_C48DABF486604D2B9F3CBC1CD01AC76D"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p> </td> 
  <td class="stentry"> <p>Número da camada de efeito (int diferente de 0). </p></td> 
 </tr> 
</table>

Todos os comandos no novo segmento são aplicados à camada de efeito especificada. Um segmento de camada de efeito é terminado pelo próximo `layer=` ou `effect=` ou no final da solicitação.

*`n`* deve ser menor que 0 para efeitos de camada externa (ou seja, efeitos atrás da camada pai) e maior que 0 para efeitos de camada interna (ou seja, efeitos dentro da camada pai). Os números das camadas de efeito não precisam ser consecutivos.

O número da camada de efeito especifica a ordem z, no caso de várias camadas de efeito para a mesma camada pai. As camadas com numeração mais alta são colocadas sobre camadas com numeração mais baixa.

As camadas de efeito podem ser anexadas a `layer=comp`.

## Propriedades {#section-e11f795deff345779ce280a82cf221ca}

Comando de camada de efeito. *`n`* não pode ser 0.

## Padrão {#section-84bbe1cfe7a94040827c994323ac59d4}

Nenhum.

## Exemplo {#section-adf2fd8edb184803a2603d7b9a6db6da}

`…&layer=5&src=/myCat/myImage&size=200,200&effect=-1&$shadow$&…`

## Consulte também {#section-573273e9e0e64103a5764075f5e50180}

[layer=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-layer.md)
