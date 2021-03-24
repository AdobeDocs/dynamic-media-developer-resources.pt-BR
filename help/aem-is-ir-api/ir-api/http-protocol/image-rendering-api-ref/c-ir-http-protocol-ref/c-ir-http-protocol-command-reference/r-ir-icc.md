---
description: Perfil de cor de saída.
solution: Experience Manager
title: icc
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---


# icc{#icc}

Perfil de cor de saída.

icc= *`profile`*[, *`renderIntent`*[,*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> perfil</span></span> </p></td> 
  <td class="stentry"> <p>Perfil de cor ICC. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderPropósito  </span> </span> </p></td> 
  <td class="stentry"> <p>percepção | relativo | saturação | Absoluto </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span> </span> </p></td> 
  <td class="stentry"> <p>1 para ativar, 0 para desativar a compensação do ponto de bloqueio. </p></td> 
 </tr> 
</table>

*`profile`* especifica o perfil de espaço de cores de saída para o qual a imagem renderizada deve ser convertida se for diferente do perfil de trabalho. *`profile`* deve ser um arquivo válido  `icc::Name` definido no mapa de perfil ICC de um catálogo de imagem ou catálogo padrão, ou um caminho relativo para um arquivo de perfil (normalmente com  [!DNL .icc]ou  [!DNL .icm] sufixo).

>[!NOTE]
>
>*`profile`* não pode incluir caracteres &#39;,&#39;, mesmo que codificados por HTTP.

*`renderIntent`* permite substituir a intenção de renderização padrão.

*`blackpointComp`* ativa a compensação de ponto de bloqueio se o perfil de saída suportar este recurso.

>[!NOTE]
>
>Nem todas as conversões de cores suportam todas as opções *`renderIntent`* e *`blackpointComp`*. Normalmente, essas configurações são honradas apenas quando o perfil de saída ICC caracteriza um dispositivo de saída, como uma impressora ou monitor. Além disso, alguns perfis de saída ICC não suportam todas as opções *`renderIntent`*.

## Propriedades {#section-b4042623a8ea40248c11b2153e5906b1}

Pode ocorrer em qualquer lugar dentro da solicitação. Um erro é retornado se o tipo de imagem for especificado com `fmt=` não corresponder a *`profile`*.

*`renderIntent`* e  *`blackpointComp`* são ignoradas se não forem compatíveis com o perfil ICC especificado.

Os perfis de dispositivo de saída CMYK têm mais probabilidade de suportar propósitos de renderização diferentes.

## Padrão {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

Se o gerenciamento de cores estiver ativado e `icc=` não for especificado, o servidor entregará a imagem convertida para o perfil de saída ( `attribute::IccProfile*`) correspondente ao tipo de imagem especificado com `fmt=`.

Se não especificado, *`renderIntent`* é herdado de `attribute::IccRenderIntent` e *`blackpointComp`* é herdado de `attribute::IccBlackPointCompensation`.

## Consulte também {#section-37ef83149fd74345956a98f633cc0294}

[Gerenciamento](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d) de cores,  [atributo::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127),  [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f),  [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [atributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [atributo::IccBlackPointCompensação](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
