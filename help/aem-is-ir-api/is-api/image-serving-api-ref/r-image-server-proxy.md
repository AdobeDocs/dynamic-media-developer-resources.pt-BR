---
description: Um proxy de servidor de imagens pode ser usado para redimensionar imagens para telefones japoneses.
seo-description: Um proxy de servidor de imagens pode ser usado para redimensionar imagens para telefones japoneses.
seo-title: proxy do servidor de imagens
solution: Experience Manager
title: proxy do servidor de imagens
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 49aa0861-9b03-4a62-8604-67e6cb7a621f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---


# Proxy do servidor de imagens{#image-server-proxy}

Um proxy de servidor de imagens pode ser usado para redimensionar imagens para telefones japoneses.

## Formato de URL {#section-2e8c40b0547c4f99874cdf502b338940}

O formato url para o proxy IS é muito semelhante às solicitações IS regulares. Todos os modificadores IS transmitidos ao proxy são transmitidos para o Servidor de imagens. Você pode encontrar informações sobre os modificadores IS na [Referência do protocolo HTTP](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e).

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## Lista do modificador específico do proxy {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Especifica a porcentagem da largura utilizável do dispositivo a ser usada como largura da imagem. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heiporcentagem =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Especifica a porcentagem da altura utilizável do dispositivo a ser usada como a altura da imagem. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Especifica a porcentagem da propriedade Mídia incorporada de limite de memória do dispositivo para limitar o tamanho da resposta. Isso só se aplica a respostas jpg. A qualidade da imagem será reduzida até que o tamanho da resposta esteja dentro da porcentagem especificada. </p></td> 
 </tr> 
</table>

## Limite de memória de imagem incorporado {#section-52f7c69ed8a341ceabf92ceee19b0f36}

Se o dispositivo tiver um limite sobre o tamanho das imagens que podem ser incorporadas em uma página da Web, o tamanho da imagem será restrito a esse tamanho, contanto que o formato de resposta seja jpg. O proxy limita as respostas a 500 MB se o dispositivo não tiver limite.

## Processamento de backend {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

O proxy baixa, verifica e carrega o arquivo de dados do Device Atlas uma vez por dia. A verificação extrai diferentes propriedades para diferentes dispositivos e os compara com os valores esperados antes de aceitar os novos dados.
