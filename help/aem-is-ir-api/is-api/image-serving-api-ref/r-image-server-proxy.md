---
description: Um proxy de servidor de imagens pode ser usado para redimensionar imagens para telefones japoneses.
solution: Experience Manager
title: Proxy do servidor de imagens
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0389a4af-a412-42eb-b7b4-716e47d623a0
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# Proxy do servidor de imagens{#image-server-proxy}

Um proxy de servidor de imagens pode ser usado para redimensionar imagens para telefones japoneses.

## Formato de URL {#section-2e8c40b0547c4f99874cdf502b338940}

O formato do URL para o proxy IS é muito semelhante às solicitações IS comuns. Qualquer modificador IS transmitido ao proxy é transmitido ao Servidor de imagens. Você pode encontrar informações sobre os modificadores IS na [Referência do Protocolo HTTP](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e).

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## Lista de modificadores específicos de proxy {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent = &lt;número&gt;</span> </p></td> 
  <td class="stentry"> <p>Especifica a porcentagem da largura utilizável do dispositivo a ser usada como largura da imagem. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heipercent = &lt;número&gt;</span> </p></td> 
  <td class="stentry"> <p>Especifica a porcentagem da altura utilizável do dispositivo a ser usada como altura da imagem. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent = &lt;número&gt;</span> </p></td> 
  <td class="stentry"> <p>Especifica a porcentagem da propriedade de Limite de Memória de Mídia Incorporada do dispositivo à qual limitar o tamanho da resposta. Isso se aplica somente a respostas jpg. A qualidade da imagem é reduzida até que o tamanho da resposta esteja dentro da porcentagem especificada. </p></td> 
 </tr> 
</table>

## Limite de memória de imagem incorporada {#section-52f7c69ed8a341ceabf92ceee19b0f36}

Se o dispositivo tiver um limite no tamanho das imagens que podem ser incorporadas em uma página da Web, o tamanho da imagem será restrito a esse tamanho, desde que o formato de resposta seja jpg. O proxy limita as respostas a 500 MB se o dispositivo não tiver limite.

## Processamento de backend {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

O proxy baixa, verifica e carrega o arquivo de dados do Device Atlas uma vez por dia. A verificação extrai diferentes propriedades para diferentes dispositivos e as compara com os valores esperados antes de aceitar os novos dados.
