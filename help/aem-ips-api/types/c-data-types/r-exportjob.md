---
description: Tipo de trabalho para permitir a exportação autorizada de arquivos carregados anteriormente.
solution: Experience Manager
title: ExportJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f0266b9f-c6e0-4843-b002-0bc068d43424
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# [!DNL ExportJob]{#exportjob}

Tipo de trabalho para permitir a exportação autorizada de arquivos carregados anteriormente.

ExportJob não oferece suporte para os seguintes tipos de ativos:

* Conjuntos de imagem
* Conjuntos de renderização
* Conjuntos de rotação
* Conjuntos de mídia
* Conjuntos de várias taxas de bits
* Conjuntos de vídeos
* eCatalogs
* Conjuntos de ofertas

<table id="table_D8F3FD30D15648BFA5B980D3DC0A5AB1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL assetHandleArray]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> tipos:HandleArray</span> </p> </td> 
   <td colname="col3" valign="top"> <p>Lista de <span class="codeph"> assetHandle</span> que devem ser exportados. Consulte <a href="../../types/c-data-types/r-handle-array.md#reference-1b93fefb5477459faf9253b54349b5f9" type="reference" format="dita" scope="local"> HandleArray</a>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL fmt]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Especifica o tipo de <span class="codeph"> export.Possible Values</span>: [orig, convert] </p> <p> 
     <ul id="ul_16EF4B14100C4C7AA464CA9CF7F11D1C"> 
      <li id="li_DAB2844CC55145C88A18A1F8EC4527F9">Se <span class="codeph"> fmt=orig</span>, os ativos serão exportados como originais </li> 
      <li id="li_07F2F8D159934D889FDC1022AB12B564">Se <span class="codeph"> fmt=convert</span>, os ativos serão convertidos para o formato especificado nos parâmetros de entrada <span class="codeph"> is_modify</span> ou <span class="codeph"> macro</span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL is_modifier]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Especifica a cadeia de caracteres da URL de renderização <span class="codeph"> ImageServer</span>, que está anexada à solicitação de conversão<span class="codeph"> do ExportJob </span>. </p> <p>Consulte a <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/homeisir.html" scope="external" format="html"> documentação do IS</a> para obter detalhes sobre como enviar os modificadores IS. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL macro]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL emailSetting]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Opção de configuração de email. Valores possíveis: </p> <p> 
     <ul id="ul_0EEDAE11B7CD4C53A6E4B2B8CB2CF730"> 
      <li id="li_F235F93828594ED78C6D464440F953FF"> <span class="codeph"> Tudo</span> </li> 
      <li id="li_59E14E7EBFA64432A5FAC15DA21A0521"> <span class="codeph"> Erro</span> </li> 
      <li id="li_BFE0B52CADD14CC1BA1AF42AB0AA1CE1"> <span class="codeph"> ErrorAndWarning</span> </li> 
      <li id="li_BE3AA67E14FB487B8B9CD6EF3D58824C"> <span class="codeph"> Conclusão do trabalho</span> </li> 
      <li id="li_409C68AD0D244975BFB86B08609E0146"> <span class="codeph"> Nenhum</span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> [!DNL clientId]</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>Especifica o endereço IP do cliente ou cliente que iniciou a solicitação de exportação. </p> <p> <p>Observação: esse parâmetro não está preenchido ativamente no momento e é estritamente reservado para uso futuro apenas. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

Para solicitações ExportJob onde `fmt=convert` e `is_modifier` e `macro` são fornecidos, o arquivo de destino respeita o formato fornecido por `macro`. Por exemplo:

```
input_file = fileToExport.jpg
is_modifer = &fmt=png
macro=$test$ 
output_file = fileToExport.tiff
```
