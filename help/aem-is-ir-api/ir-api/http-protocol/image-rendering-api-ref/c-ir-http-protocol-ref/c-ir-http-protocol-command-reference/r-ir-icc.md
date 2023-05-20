---
title: icc
description: Perfil de cores de saída.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39b25f7c-ed3c-4132-8241-e7f3aab07b00
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# icc{#icc}

Perfil de cores de saída.

icc= *`profile`*[, *`renderIntent`*[,*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> perfil</span></span> </p></td> 
  <td class="stentry"> <p>Perfil de cores ICC. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent </span> </span> </p></td> 
  <td class="stentry"> <p>perceptivo | relativo | saturação | absoluto </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span> </span> </p></td> 
  <td class="stentry"> <p>1 para ativar, 0 para desativar a compensação de ponto de bloqueio. </p></td> 
 </tr> 
</table>

*`profile`* Especifica o perfil do espaço de cores de saída no qual a imagem renderizada deve ser convertida se for diferente do perfil de trabalho. *`profile`* Deve ser um válido `icc::Name` definido no mapa de perfis ICC de um catálogo de imagens ou catálogo padrão, ou um caminho relativo para um arquivo de perfil (normalmente com [!DNL `.icc`] ou [!DNL `.icm`] sufixo).

>[!NOTE]
>
>*`profile`* Não pode incluir caracteres &#39;,&#39;, mesmo se codificados em HTTP.

*`renderIntent`* Permite substituir a tentativa de renderização padrão.

*`blackpointComp`* Ativa a compensação de pontos negros se o perfil de saída suportar esse recurso.

>[!NOTE]
>
>Nem todas as conversões de cores dão suporte a tudo *`renderIntent`* e *`blackpointComp`* opções. Normalmente, essas configurações são respeitadas apenas quando o perfil de saída ICC caracteriza um dispositivo de saída, como uma impressora ou monitor. Além disso, alguns perfis de saída ICC não suportam todos *`renderIntent`* opções.

## Propriedades {#section-b4042623a8ea40248c11b2153e5906b1}

Pode ocorrer em qualquer lugar na solicitação. Um erro é retornado se o tipo de imagem for especificado com `fmt=` não corresponde *`profile`*.

Ambos *`renderIntent`* e *`blackpointComp`* são ignorados se não forem compatíveis com o perfil ICC especificado.

Os perfis de dispositivo de saída CMYK têm mais probabilidade de suportar diferentes intenções de renderização.

## Padrão {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

Se o gerenciamento de cores estiver ativado e `icc=` não for especificado, o servidor fornecerá a imagem convertida no perfil de saída ( `attribute::IccProfile*`) correspondente ao tipo de imagem especificado com `fmt=`.

Se não especificado, *`renderIntent`* é herdado de `attribute::IccRenderIntent`, e *`blackpointComp`* é herdado de `attribute::IccBlackPointCompensation`.

## Consulte também {#section-37ef83149fd74345956a98f633cc0294}

[Gerenciamento de cores](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d), [attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f), [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
