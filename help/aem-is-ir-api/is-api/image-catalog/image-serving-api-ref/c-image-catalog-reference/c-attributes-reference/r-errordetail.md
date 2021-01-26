---
description: Detalhes da mensagem de erro. Especifica o nível de detalhes das mensagens de erro retornadas via HTTP como o valor error.message.
solution: Experience Manager
title: ErrorDetail
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---


# ErrorDetail{#errordetail}

Detalhes da mensagem de erro. Especifica o nível de detalhes das mensagens de erro retornadas via HTTP como o valor error.message.

São permitidos os seguintes valores:

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Somente título. Retorna uma breve descrição geral do erro. Recomendado para servidores ao vivo que podem ser acessados publicamente. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Breve mensagem. Reservado para uso futuro. Atualmente retorna as mesmas informações de 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Mensagem detalhada. Fornece detalhes no nível do usuário sobre o erro. Pode incluir informações confidenciais, como caminhos de arquivo. Recomendado para servidores de armazenamento temporário, controle de qualidade e desenvolvimento de aplicativos. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Informações completas de depuração. Adiciona rastreamentos de pilha Java quando aplicável. As imagens de erro nunca incluem rastreamentos de pilha e, em vez disso, retornam informações de nível 2 em <span class="codeph"> $error.message</span>. Essas informações podem ser úteis quando há problemas de relatórios no suporte técnico da Dynamic Media. </p></td> 
 </tr> 
</table>

## Propriedades {#section-e167895723ca4ad4ba283d3d7b4324de}

O valor enumerado deve ser 0, 1, 2 ou 3.

## Padrão {#section-8f27098e509945a18676aca0675c8f41}

Herdado de `default::ErrorDetail` se não for especificado ou se estiver vazio.

## Consulte também {#section-5451b0525ed74121950bfc34726c3970}

[atributo::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
