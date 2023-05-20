---
title: ErrorDetail
description: Detalhes da mensagem de erro. Especifica o nível de detalhes das mensagens de erro retornadas via HTTP como o valor error.message.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39d7fc44-7605-4f93-b2f9-0a6e8bc76ec7
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 2%

---

# ErrorDetail{#errordetail}

Detalhes da mensagem de erro. Especifica o nível de detalhes das mensagens de erro retornadas via HTTP como o valor error.message.

## Título {#section-c10d75d72ee24d16a67cc8d927f1deba}

Os seguintes valores são permitidos:

<table id="simpletable_7904444FF9F14D678F05094CA9E45664"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Somente título. Retorna uma breve descrição geral do erro. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Mensagem breve. Reservado para uso futuro. Atualmente retorna as mesmas informações que 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Mensagem detalhada. Fornece detalhes no nível do usuário sobre o erro. Pode incluir informações confidenciais, como caminhos de arquivos. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Informações completas de depuração. Adiciona rastreamentos de pilha Java™ quando aplicável. As imagens com erro nunca incluem rastreamentos de pilha e, em vez disso, retornam informações de nível 2 em <span class="codeph"> $error.message</span>. </p></td> 
 </tr> 
</table>

* O nível 0 é recomendado para servidores em tempo real que podem ser acessados publicamente.
* O nível 2 é recomendado para servidores de preparo, controle de qualidade e desenvolvimento de aplicativos.
* As informações de nível 3 podem ser úteis quando problemas forem relatados ao suporte técnico da Dynamic Media.

## Propriedades {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

Valor enumerado, deve ser 0, 1, 2 ou 3.

## Padrão {#section-5e78d550050840cc9a1de811c581b94f}

Herdado de `default::ErrorDetail` se não especificado ou se estiver vazio.

## Consulte também {#section-474e71922d194c7ca06f2aad3b30e025}

[attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
