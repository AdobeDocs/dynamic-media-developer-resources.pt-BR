---
description: nulo
seo-description: nulo
seo-title: Retornos de chamada de Evento
solution: Experience Manager
title: Retornos de chamada de Evento
topic: Dynamic media
uuid: 4a3dc8d7-2eb3-4244-849b-01d1314e43f2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Retornos de chamada de Evento{#event-callbacks}

O visualizador suporta retornos de chamada do evento JavaScript que a página da Web usa para rastrear o processo de inicialização do visualizador ou o comportamento do tempo de execução.

Os manipuladores de retorno de chamada são atribuídos transmitindo nomes de eventos e funções de manipulador correspondentes com a `handlers` propriedade para o objeto `config` JSON no construtor do visualizador. Como alternativa, é possível usar o método `setHandlers()` API.

Os eventos do visualizador suportados incluem:

<table id="table_D4A2035B65B140F882F550B711BD3160"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>evento do visualizador </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> initComplete </span> </p> </td> 
   <td colname="col2"> <p>Aciona quando a inicialização do visualizador é concluída e todos os componentes internos são criados, para que seja possível usar a API <span class="codeph"> getComponent() </span> . O manipulador de retorno de chamada não aceita nenhum argumento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> trackEvent </span> </p> </td> 
   <td colname="col2"> <p> Aciona cada vez que um evento ocorre dentro do visualizador que pode ser manipulado por um sistema de rastreamento de eventos, como o Adobe Analytics. O manipulador de retorno de chamada aceita os seguintes argumentos: </p> <p> 
     <ul id="ul_8A5F409E32E94063AE8D3AB158A0E13D"> 
      <li id="li_1311D5DDD4454FBC9116BA8E2CB003B1"> <p> <span class="codeph"> objID {String} </span> - não usado no momento. </p> </li> 
      <li id="li_C2ABD13097FA40A7B9801C0B7592FB59"> <p> <span class="codeph"> compClass {String} </span> - não usado no momento. </p> </li> 
      <li id="li_3BE8001365714C3FAC32C9B2CFFD5DCE"> <p> <span class="codeph"> instName {String} </span> - um nome de instância do componente SDK do visualizador que disparou o evento. </p> </li> 
      <li id="li_755DDE84B1CC4B4D8A3FA0C774CBA666"> <p> <span class="codeph"> timeStamp {Number} </span> - carimbo de data e hora do evento. </p> </li> 
      <li id="li_05A1C45826AC4D1192CB72FE07EE4C29"> <p> <span class="codeph"> eventInfo {String} </span> - carga do evento. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> quickViewActivate </span> </p> </td> 
   <td colname="col2"> <p> Aciona quando o usuário ativa um ponto de acesso com dados de Visualização Rápida associados a ele. O manipulador de retorno de chamada utiliza o seguinte argumento: </p> <p> 
     <ul id="ul_171110934BD54839B371FAD8D2AD467B"> 
      <li id="li_7B14C3BA432B43E392AC103926807E88"> <p> <span class="codeph"> data {Object} </span> - um objeto JSON que contém dados da definição do ponto de acesso. O <span class="codeph"> sku de campo </span> é obrigatório enquanto outros campos são opcionais e dependem da definição do ponto de acesso de origem. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Consulte também [InterativeImage](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-interactiveimage.md#reference-bd16cadc0c054fafb0db4994741d47cd) e [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
