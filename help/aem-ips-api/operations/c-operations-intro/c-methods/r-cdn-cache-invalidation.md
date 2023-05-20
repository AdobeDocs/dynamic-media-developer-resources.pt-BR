---
description: Encaminha a lista de URLs fornecida ao provedor Dynamic Media CDN (Content Distribution Network) para invalidar o cache existente de respostas HTTP.
solution: Experience Manager
title: cdnCacheInvalidation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 65b758f2-b49a-4616-b657-a64808c9202a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---

# cdnCacheInvalidation{#cdncacheinvalidation}

Encaminha a lista de URLs fornecida ao provedor Dynamic Media CDN (Content Distribution Network) para invalidar o cache existente de respostas HTTP.

## cdnCacheInvalidation: Sobre {#section-4f70d2bc79d64288b961836ab17e9690}

A invalidação do cache do CDN força todas as solicitações HTTP para esses URLs a serem revalidados em relação aos dados publicados atuais na rede do Dynamic Media depois que essa solicitação de invalidação for processada pela rede CDN. Qualquer URL que não esteja conectado à estrutura de URL de serviço do Dynamic Media e que corresponda diretamente à ID raiz da empresa do Dynamic Media atribuída quando a empresa foi criada resultará em uma falha de API para toda a solicitação. Quaisquer URLs inválidos que a CDN não aceite e que considere inválidos também resultarão em uma falha de API para toda a solicitação.

**Frequência de uso: regras**

As regras que regem a frequência de uso desse recurso são controladas pelos parceiros CDN do Dynamic Media. A CDN mantém a discrição de degradar a capacidade de resposta dessas invalidações para manter o desempenho ideal de seu serviço para seus usuários. Se a Dynamic Media for notificada de uso excessivo desse recurso, precisaremos recorrer à desativação do recurso por empresa ou inteiramente por todo o serviço.

**Emails de confirmação**

Os emails de confirmação do parceiro de CDN da Dynamic Media podem ser enviados ao criador da lista ou até 5 outros endereços de email. A API envia a confirmação quando toda a rede CDN é notificada de que os URLs referenciados no email foram apagados. Uma única chamada para `cdnCacheInvalidation` O pode enviar vários emails se o número de URLs fornecidos exceder o número que o Dynamic Media pode entregar ao parceiro de CDN em uma única notificação. Atualmente, isso acontece se a solicitação exceder 100 URLs, mas estiver sujeita a alterações com base na solicitação do parceiro de CDN.

**Compatível desde**

6.0

## Tipos de usuário autorizados {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## Parâmetros {#section-bd1ed2b7419945d19a2ebd5668499f72}

**Entrada** ( `cdnCacheInvalidationParam`)

<table id="table_EDD1875264C846BE951869D528A90D73"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Nome</b> </th> 
   <th class="entry"> <b> Tipo</b> </th> 
   <th class="entry"> <b> Obrigatório</b> </th> 
   <th class="entry"> <b> Descrição</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td> <p> Sim </p> </td> 
   <td> <p> O identificador da empresa conectada com os URLs a serem invalidados. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> tipos:UrlArray</span> </p> </td> 
   <td> <p> Sim </p> </td> 
   <td> <p> Lista de até 1000 URLs a serem invalidados do cache da CDN. Todos os URLS devem conter a ID raiz da empresa do Dynamic Media para serem invalidados. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output**( `cdnCacheInvalidationReturn`)

<table id="table_1D947C1BF8864820AD7BA0CDC0F076F9"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Nome</b> </th> 
   <th class="entry"> <b> Tipo</b> </th> 
   <th class="entry"> <b> Obrigatório</b> </th> 
   <th class="entry"> <b> Descrição</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> invalidationHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Sim </p> </td> 
   <td colname="col4"> <p>Um identificador que faz referência à solicitação de limpeza. </p> <p>A variável <span class="codeph"> cdnCacheInvalidation</span> A API agora invalida o cache quase imediatamente (~5 segundos). Dessa forma, a pesquisa do status de invalidação geralmente não é mais necessária. </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> estimatedSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Sim </p> </td> 
   <td colname="col4"> <p>Segundos estimados para a conclusão da solicitação de limpeza. Os clientes devem aguardar esse tempo antes de pesquisar o status. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section-f414361a58e84dfcbbac30a358d02125}

Esse exemplo solicita quatro URLs a serem invalidados no cache da CDN. A resposta contém contagens resumidas do sucesso das operações e uma lista de detalhes de erros fornecidos diretamente da CDN para ajudar o cliente a usar esse recurso.

`getCdnCacheInvalidationStatus` operação.

**Solicitação**

```java
<cdnCacheInvalidationParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <companyHandle>c|6</companyHandle>
   <urlArray>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$thumbnail$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$product$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$large$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/ImageSetConfigDefaults?req=userdata</items>
    </urlArray>
</cdnCacheInvalidationParam>
```

**Resposta**

```java
<cdnCacheInvalidationReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</cdnCacheInvalidationReturn>
```
