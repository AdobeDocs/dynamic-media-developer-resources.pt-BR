---
description: Contém [!DNL Platform Server] configurações.
solution: Experience Manager
title: PlatformServer.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 00d55453-e7e6-4242-be83-7efa12764e5d
TQID: 'https://experienceleague.adobe.com/DpX2C7E58x30jn3W4mQSJS9FDlbZgQl0xJgtkppxePk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 155
ht-degree: 0%

---

# PlatformServer.conf{#platformserver-conf}

Contém configurações de [!DNL Platform Server].

Este arquivo é um arquivo de propriedades JAVA. Tenha cuidado ao seguir as convenções apropriadas; caso contrário, o [!DNL Platform Server] pode falhar ao iniciar. Use uma barra invertida dupla &#39;\\&#39; ou uma barra invertida simples &#39;/&#39; em vez de uma barra invertida &#39;\&#39; nos caminhos de arquivo do Windows. A barra invertida é usada como um caractere de escape neste tipo de arquivo.

As alterações feitas neste arquivo entrarão em vigor depois que ele for salvo.

Somente as configurações listadas abaixo podem ser alteradas em [!DNL PlatformServer.conf]. Se uma configuração específica estiver ausente, ela poderá ser adicionada em qualquer lugar no arquivo. Somente uma instância de cada configuração pode estar presente.

<table id="simpletable_38244750F50A46E5B0077F5F860B125C"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Configurações gerais de [!DNL Platform Server] </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cache.rootPaths=./cache </span> </p> <p> <span class="codeph"> cache.maxEntries=1000000 </span> </p> <p> <span class="codeph"> cache.maxSize=1073741824 </span> </p> <p> <span class="codeph"> isConnection.port=27345 </span> </p> <p> <span class="codeph"> allowDefaultCatalogRequsts=true </span> </p> <p> <span class="codeph"> saveToFile.saveTimeout=60000 </span> </p> <p> <span class="codeph"> staticContent.rootPaths=./static-content </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Configuração de cluster de cache </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cluster.hosts=&lt;vazio&gt; </span> </p> <p> <span class="codeph"> cacheCluster.queryTimeout=50 </span> </p> <p> <span class="codeph"> cacheCluster.fetchTimeout=10000 </span> </p> <p> <span class="codeph"> cacheCluster.updateLocalCache=true </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Configuração de redirecionamento de erro </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> errorRedirect.rootUrl=&lt;empty&gt; </span> </p> <p> <span class="codeph"> errorRedirect.connectTimeout=1000 </span> </p> <p> <span class="codeph"> errorRedirect.socketTimeout=30000 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Configuração do SVG </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> svgProvider.rootPaths=./images </span> </p> <p> <span class="codeph"> svgProvider.SVGFileSizeLimit=1024 </span> </p> <p> <span class="codeph"> svgProvider.port=8080 </span> </p> <p> <span class="codeph"> svgProvider.fontRoot=./images </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Respostas do conjunto de mdias </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fvctx.useCatalogRecordValidation=false </span> </p> <p> <span class="codeph"> fvctx.nestedLimit=10 </span> </p> <p> <span class="codeph"> fvctx.brochureLimit=20 </span> </p> </td> 
 </tr> 
</table>
