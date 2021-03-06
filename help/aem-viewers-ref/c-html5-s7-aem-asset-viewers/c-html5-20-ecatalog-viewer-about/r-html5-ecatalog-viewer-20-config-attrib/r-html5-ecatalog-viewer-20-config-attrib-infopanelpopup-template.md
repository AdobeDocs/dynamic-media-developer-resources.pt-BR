---
title: InfoPanelPopup.template
description: InfoPanelPopup.template
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 20618017-2f73-4951-baa9-2063a0f4efcb
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# InfoPanelPopup.template{#infopanelpopup-template}

` [InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`modelo`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> modelo</span></span> </p> </td> 
   <td> <p>O modelo de conteúdo no qual os dados retornados do servidor de informações são mesclados. </p> <p>O modelo de conteúdo é um XML seguindo este DTD: </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;[
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      ]&gt;</code> </p> <p>A sintaxe real para o modelo de conteúdo é a seguinte: </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]]&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]]&gt;
      &lt;/info&gt;</code> </p> <p>Ou seja, o template deve começar com a variável <span class="codeph"> &lt;info&gt;</span> elemento que pode conter o padrão opcional <span class="codeph"> &lt;var&gt;</span> elementos. O próprio conteúdo do modelo, <span class="codeph"> TEMPLATE_CONTENT</span> é texto HTML. Além disso, o template de conteúdo pode conter nomes de variáveis delimitados por <span class="codeph"> $</span> caracteres que são substituídos pelos valores da variável retornados pelo servidor de informações ou pelos valores padrão. </p> <p>As variáveis padrão definidas no modelo podem ser globais (se o atributo de sobreposição não estiver definido) ou específicas para uma determinada chave de sobreposição (se o atributo de sobreposição estiver presente). </p> <p>Durante o processamento do modelo, as variáveis específicas para sobrepor as chaves têm prioridade sobre as variáveis globais. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Ao configurar o Pop-up do painel Informações, o código do HTML e o código JavaScript passados para o Painel Informações são executados no computador do cliente. Portanto, verifique se esse código HTML e o código JavaScript estão protegidos.

## Propriedades {#section-6dd7785357d740d095fa9f7fd0f67da4}

Opcional.

## Padrão {#section-cd5db06d08aa4de49e37d6c938b41570}

Nenhum.

## Exemplo {#section-16d184665c484964af9a22f79ff3f840}

Supondo que a resposta do servidor de informações retorne o nome do produto como variável `$1$` e o URL da imagem do produto é retornado como variável `$2$`.

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
