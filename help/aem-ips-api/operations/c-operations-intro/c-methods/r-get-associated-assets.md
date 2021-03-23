---
description: Obtém ativos associados a um ativo especificado e detalhes sobre seu relacionamento.
seo-description: Obtém ativos associados a um ativo especificado e detalhes sobre seu relacionamento.
seo-title: getAssociatedAssets
solution: Experience Manager
title: getAssociatedAssets
uuid: 70c2f8aa-9104-42b0-b85b-14f90f1ead52
feature: Dynamic Media Classic, SDK/API, Gerenciamento de ativos
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---


# getAssociatedAssets{#getassociatedassets}

Obtém ativos associados a um ativo especificado e detalhes sobre seu relacionamento.

Sintaxe

## Tipos de usuário autorizados {#section-453cc706400345778713cda249bfac16}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-d11d0dab59e94e89b466123a0ebfa82e}

**Entrada (getAssociatedAssetsParam)**

<table id="table_DBB97A6507EB48479FFFD2184FF8F07C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obrigatório </p> </th> 
   <th colname="col4" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sim </p> </td> 
   <td colname="col4"> <p>Lidar com a empresa proprietária do ativo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sim </p> </td> 
   <td colname="col4"> <p>Identificador de ativo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:StringArray</span> </p> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>A matriz de campos de resposta desejada. Consulte resposta - FieldArray/excludeFieldArray na Introdução. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:StringArray</span> </p> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>A matriz de campos de resposta excluídos. Consulte resposta - FieldArray/excludeFieldArray na Introdução. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Saída (getAssociatedAssetsReturn)**

<table id="table_B894B4B6EFA24359A0250A8A4523EA8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obrigatório </p> </th> 
   <th colname="col4" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> containerArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AssetArray</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Matriz de ativos de conjunto e modelo contendo o ativo especificado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AssetArray</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Matriz de ativos contidos pelo conjunto ou ativo de modelo especificado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> layerReferenceArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AssetArray</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Matriz de ativos referenciados em uma camada ou URL de modelo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ownerArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AssetArray</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Matriz de ativos proprietários do ativo especificado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> derivadoArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AssetArray</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Matriz de ativos que foram usados para gerar o ativo especificado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generatorArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>O <span class="codeph"> geradorArray</span> lista a forma como esse ativo foi criado. Por exemplo, se <span class="codeph"> assetHandler</span> fosse uma página de imagem de um PDF, isso conteria a ferramenta do processador PDF e referenciaria o ativo PdfFile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generatedArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>O <span class="codeph"> generatedArray</span> inverte a forma como esse ativo foi criado. Por exemplo, o <span class="codeph"> generatedArray</span> poderia conter a lista de imagens geradas a partir desse <span class="codeph"> assetHandler</span> se esse fosse um ativo PdfFile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAsset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:Ativo</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>As informações do ativo em miniatura associadas ao ativo de solicitação. Se nenhum ativo em miniatura for atribuído, o campo será omitido na resposta. </p> </td> 
  </tr> 
 </tbody> 
</table>

Você pode usar os parâmetros `responseFieldArray` ou `excludeFieldArray` para limitar o tamanho da resposta. Em particular, os itens `GenerationInfo` retornados no `generatorArray` ou `generatedArray` padrão para incluir o originador e os registros de ativos gerados. Para um tipo de ativo PDF, esse comportamento resulta em várias cópias indesejadas do registro de ativo PDF &quot;originador&quot; na resposta. Você pode eliminar esse problema adicionando `generatedArray/items/originator` a `excludeFieldArray`. Ou você pode especificar uma lista explícita de campos de resposta que deseja incluir em `responseFieldArray`.

## Exemplos {#section-8946ea4b9cb94912a8408249c897f192}

O exemplo básico a seguir é uma solicitação para o identificador do gerador para uma imagem extraída de um PDF. Inclui um `containerArray` de comprimento um com um item incluindo o `assetHandle` do PDF.

**Solicitação**

```java
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:beta="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
   <soap:Body>
      <beta:getAssociatedAssetsParam>
         <beta:companyHandle>c|11</beta:companyHandle>
         <beta:assetHandle>a|197</beta:assetHandle>
         <beta:responseFieldArray>
            <beta:items>containerArray/items/assetHandle</beta:items>
         </beta:responseFieldArray>
      </beta:getAssociatedAssetsParam>
   </soap:Body>
</soap:Envelope>
```

**Resposta**

```java
<soapenv:Envelope xmlns:soapenv="http://www.w3.org/2003/05/soap-envelope">
   <soapenv:Body>
      <getAssociatedAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
         <containerArray>
            <items>
               <assetHandle>a|207</assetHandle>
            </items>
         </containerArray>
      </getAssociatedAssetsReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

O inverso do exemplo acima é o seguinte:

**Solicitação**

```java
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:beta="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
   <soap:Body>
      <beta:getAssociatedAssetsParam>
         <beta:companyHandle>c|11</beta:companyHandle>
         <beta:assetHandle>a|177</beta:assetHandle>
        <beta:responseFieldArray>
           <beta:items>generatedArray/items/originator/assetHandle</beta:items>
         </beta:responseFieldArray>
      </beta:getAssociatedAssetsParam>
   </soap:Body>
</soap:Envelope>
```

**Resposta**

```java
<soapenv:Envelope xmlns:soapenv="http://www.w3.org/2003/05/soap-envelope">
   <soapenv:Body>
      <getAssociatedAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
         <generatedArray>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
         </generatedArray>
      </getAssociatedAssetsReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

Neste próximo exemplo, um grupo é adicionado a uma empresa com `groupHandleArray`. Este exemplo usa apenas um grupo.

**Solicitação**

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**Resposta**

Nenhum.
