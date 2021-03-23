---
description: Encaminha a lista de URLs fornecida para o provedor CDN (Content Distribution Network) da Dynamic Media para invalidar seu cache existente de respostas HTTP.
solution: Experience Manager
title: cdnCacheInvalidation
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---


# cdnCacheInvalidation{#cdncacheinvalidation}

Encaminha a lista de URLs fornecida para o provedor CDN (Content Distribution Network) da Dynamic Media para invalidar seu cache existente de respostas HTTP.

## cdnCacheInvalidation: Sobre {#section-4f70d2bc79d64288b961836ab17e9690}

A invalidação do cache CDN força todas as solicitações HTTP para esses URLs serem revalidadas em relação aos dados publicados atuais na rede Dynamic Media depois que essa solicitação de invalidação é processada pela rede CDN. Todos os URLs que não estão conectados à estrutura de URL do serviço Dynamic Media e correspondem diretamente à ID raiz da empresa Dynamic Media atribuída quando a empresa é criada resultarão em uma falha de API para toda a solicitação. Todos os URLs inválidos que a CDN não suporta e que considera inválidos também resultarão em uma falha da API para toda a solicitação.

**Frequência de utilização: Regras**

As regras que regem a frequência do uso desse recurso são controladas pelos parceiros CDN do Dynamic Media. A CDN mantém a discrição para degradar a capacidade de resposta dessas invalidações para manter o desempenho ideal do seu serviço para seus usuários. Caso a Dynamic Media seja notificada sobre o uso excessivo desse recurso, precisaremos usar a desativação do recurso por empresa ou totalmente pelo serviço.

**Emails de confirmação**

Os emails de confirmação do parceiro CDN do Dynamic Media podem ser enviados para o criador da lista ou até 5 outros endereços de email. A API envia a confirmação quando toda a rede CDN foi notificada de que os URLs referenciados no email foram apagados. Uma única chamada para `cdnCacheInvalidation` pode enviar vários emails se o número de URLs fornecidas exceder o número que a Dynamic Media pode fornecer ao parceiro CDN em uma única notificação. Atualmente, isso seria se a solicitação excedesse 100 URLs, mas está sujeita a alterações com base na solicitação do parceiro da CDN.

**Suportado desde**

6,0

## Tipos de usuário autorizados {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## Parâmetros {#section-bd1ed2b7419945d19a2ebd5668499f72}

**Entrada** (  `cdnCacheInvalidationParam`)

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
   <td> <p> O identificador da empresa conectada aos URLs para invalidar. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> tipos:UrlArray</span> </p> </td> 
   <td> <p> Sim </p> </td> 
   <td> <p> Lista de até 1000 URLs para invalidar do cache CDN. Todos os URLS devem conter a ID raiz da empresa do Dynamic Media para serem invalidados. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Saída**(  `cdnCacheInvalidationReturn`)

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
   <td colname="col4"> <p>Um identificador que faz referência à solicitação de limpeza. </p> <p>A API <span class="codeph"> cdnCacheInvalidation</span> agora invalida o cache quase imediatamente (~5 segundos). Dessa forma, a pesquisa por status de invalidação geralmente não é mais necessária. </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> estimatedSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Sim </p> </td> 
   <td colname="col4"> <p>Segundos estimados para a conclusão da solicitação de limpeza. Os clientes devem aguardar por esse tempo antes de pesquisar o status. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section-f414361a58e84dfcbbac30a358d02125}

Este exemplo solicita que quatro URLs sejam invalidadas no cache CDN. A resposta contém contagens resumidas do sucesso das operações e uma lista de detalhes de erro fornecidos diretamente da CDN para ajudar o cliente a usar esse recurso.

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

