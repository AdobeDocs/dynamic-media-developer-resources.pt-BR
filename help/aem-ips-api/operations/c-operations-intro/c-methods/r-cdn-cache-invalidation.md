---
description: Encaminha a lista de URLs fornecida para o provedor Dynamic Media CDN (Content Distribution Network) para invalidar o cache existente de respostas HTTP.
solution: Experience Manager
title: cdnCacheInvalidation
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---


# cdnCacheInvalidation{#cdncacheinvalidation}

Encaminha a lista de URLs fornecida para o provedor Dynamic Media CDN (Content Distribution Network) para invalidar o cache existente de respostas HTTP.

## cdnCacheInvalidation: Sobre {#section-4f70d2bc79d64288b961836ab17e9690}

A invalidação do cache CDN força todas as solicitações HTTP para esses URLs a serem revalidados em relação aos dados publicados atuais na rede Dynamic Media após essa solicitação de invalidação ser processada pela rede CDN. Quaisquer URLs que não estejam conectados à estrutura do URL do serviço Dynamic Media e que correspondam diretamente à ID raiz da empresa Dynamic Media atribuída quando a empresa é criada resultarão em uma falha da API para toda a solicitação. Quaisquer URLs inválidos que o CDN não suporta e que considere inválidos também resultarão em uma falha de API para toda a solicitação.

**Frequência de utilização: Regras**

As regras que regulam a frequência de uso desse recurso são controladas pelos parceiros CDN do Dynamic Media. O CDN mantém a discrição de diminuir a capacidade de resposta dessas invalidações para manter o desempenho ótimo de seu serviço para seus usuários. Se a Dynamic Media for notificada de uso excessivo deste recurso, será necessário desativar o recurso por empresa ou totalmente pelo serviço.

**E-mails de confirmação**

Os emails de confirmação do parceiro Dynamic Media CDN podem ser enviados para o criador da lista ou até cinco outros endereços de email. A API envia a confirmação quando toda a rede CDN foi notificada de que os URLs referenciados no email foram apagados. Uma única chamada para `cdnCacheInvalidation` pode enviar vários emails se o número de URLs fornecidos exceder o número que a Dynamic Media pode fornecer ao parceiro CDN em uma única notificação. Atualmente, isso ocorre se a solicitação exceder 100 URLs, mas está sujeita a alterações com base na solicitação do parceiro CDN.

**Suportado desde**

6,0

## Tipos de usuário autorizados {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## Parâmetros {#section-bd1ed2b7419945d19a2ebd5668499f72}

**Input** (  `cdnCacheInvalidationParam`)

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
   <td> <p> O identificador da empresa conectada aos URLs a serem invalidados. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> tipos:UrlArray</span> </p> </td> 
   <td> <p> Sim </p> </td> 
   <td> <p> Lista de até 1000 URLs para invalidar do cache CDN. Todos os URLS devem conter a ID raiz da empresa Dynamic Media a ser invalidada. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output**(  `cdnCacheInvalidationReturn`)

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
   <td colname="col4"> <p>Um identificador que faz referência à solicitação de expurgação. </p> <p>A API <span class="codeph"> cdnCacheInvalidation</span> agora invalida o cache quase imediatamente (~5 segundos). Dessa forma, a pesquisa para o status de invalidação geralmente não é mais necessária. </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> estimatedSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Sim </p> </td> 
   <td colname="col4"> <p>Estimados segundos para a conclusão da solicitação de expurgação. Os clientes devem aguardar esse tempo antes do status da pesquisa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section-f414361a58e84dfcbbac30a358d02125}

Este exemplo solicita que quatro URLs sejam invalidados no cache de CDN. A resposta contém contagens resumidas do sucesso das operações e uma lista de detalhes de erros fornecidos diretamente da CDN para ajudar o cliente a usar esse recurso.

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

