---
description: Detalhes da mensagem de erro. Especifica o nível de detalhes das mensagens de erro retornadas via HTTP como o valor error.message.
seo-description: Detalhes da mensagem de erro. Especifica o nível de detalhes das mensagens de erro retornadas via HTTP como o valor error.message.
seo-title: ErrorDetail
solution: Experience Manager
title: ErrorDetail
topic: Dynamic Media Image Serving - Image Rendering API
uuid: aab11640-95d7-427d-b79f-c477b2c9047e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# ErrorDetail{#errordetail}

Detalhes da mensagem de erro. Especifica o nível de detalhes das mensagens de erro retornadas via HTTP como o valor error.message.

## Título {#section-c10d75d72ee24d16a67cc8d927f1deba}

São permitidos os seguintes valores:

<table id="simpletable_7904444FF9F14D678F05094CA9E45664"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Somente título. Retorna uma breve descrição geral do erro. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Breve mensagem. Reservado para uso futuro. Atualmente retorna as mesmas informações de 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Mensagem detalhada. Fornece detalhes no nível do usuário sobre o erro. Pode incluir informações confidenciais, como caminhos de arquivo. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Informações completas de depuração. Adiciona rastreamentos de pilha Java quando aplicável. As imagens de erro nunca incluem rastreamentos de pilha e, em vez disso, retornam informações de nível 2 em <span class="codeph"> $error.message</span>. </p></td> 
 </tr> 
</table>

* O nível 0 é recomendado para servidores ao vivo que possam ser acessados publicamente.
* O Nível 2 é recomendado para servidores de armazenamento temporário, garantia de qualidade e desenvolvimento de aplicativos.
* As informações de nível 3 podem ser úteis quando há problemas de relatórios no suporte técnico da Dynamic Media.

## Propriedades {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

O valor enumerado deve ser 0, 1, 2 ou 3.

## Padrão {#section-5e78d550050840cc9a1de811c581b94f}

Herdado de `default::ErrorDetail` se não for especificado ou se estiver vazio.

## Consulte também {#section-474e71922d194c7ca06f2aad3b30e025}

[atributo::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
