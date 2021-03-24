---
description: Um proxy do servidor de imagens pode ser usado para redimensionar imagens para telefones japoneses.
solution: Experience Manager
title: Proxy do servidor de imagens
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---


# Proxy do servidor de imagens{#image-server-proxy}

Um proxy do servidor de imagens pode ser usado para redimensionar imagens para telefones japoneses.

## Formato de URL {#section-2e8c40b0547c4f99874cdf502b338940}

O formato de url do proxy IS é muito semelhante a solicitações IS comuns. Qualquer modificador IS transmitido ao proxy é passado para o Servidor de Imagem. Você pode encontrar informações sobre os modificadores IS no [Referência do Protocolo HTTP](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e).

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## Lista de modificadores específicos de proxy {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Especifica a porcentagem da largura utilizável do dispositivo a ser usada como a largura da imagem. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heipercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Especifica a porcentagem da altura utilizável do dispositivo a ser usada como a altura da imagem. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Especifica a porcentagem da propriedade de Mídia incorporada de limite de memória do dispositivo para limitar o tamanho da resposta. Isso só será aplicado às respostas jpg. A qualidade da imagem será reduzida até que o tamanho da resposta esteja dentro da porcentagem especificada. </p></td> 
 </tr> 
</table>

## Limite de memória de imagem incorporada {#section-52f7c69ed8a341ceabf92ceee19b0f36}

Se o dispositivo tiver um limite sobre o tamanho das imagens que podem ser incorporadas em uma página da Web, o tamanho da imagem será restrito a esse tamanho, desde que o formato de resposta seja jpg. O proxy limita as respostas a 500 MB se o dispositivo não tiver limite.

## Processamento de backend {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

O proxy baixa, verifica e carrega o arquivo de dados do Device Atlas uma vez por dia. A verificação extrai propriedades diferentes para dispositivos diferentes e as compara com valores esperados antes de aceitar os novos dados.
