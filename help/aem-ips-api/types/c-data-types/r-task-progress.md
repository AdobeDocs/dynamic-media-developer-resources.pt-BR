---
description: Informações de progresso da Tarefa.
seo-description: Informações de progresso da Tarefa.
seo-title: TaskProgress
solution: Experience Manager
title: TaskProgress
topic: Scene7 Image Production System API
uuid: b3b67803-147a-48a3-acc3-d608e01e0800
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TaskProgress{#taskprogress}

Informações de progresso da Tarefa.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskType</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Descrição do tipo de Tarefa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcessed</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Número de itens de tarefa já processados. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numProcessing</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Número de itens de tarefa em andamento. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> numCurrent</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Número de itens de tarefa pendentes (ainda não processados). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progresso</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:duplo</span> </td> 
   <td colname="col3"> % progresso (intervalo 0.0 - 1.0). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> progressMessage</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Mensagem de progresso. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastProgressUpdate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Hora em que as últimas informações de progresso foram atualizadas pela última vez. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskItemProgressArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:TaskItemProgressArray</span> </td> 
   <td colname="col3"> Matriz de itens de tarefa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> taskState</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Os valores incluem: 
    <ul id="ul_BD00DC855B1D42748204E8BCA81FD4BF">
     <li id="li_01FE691763B3465DBF3402E7CDEA50C3"><span class="codeph"> Desconhecido</span>: Quando o monitor de tarefa transição entre estados. </li>
     <li id="li_AA2D1F9ADDE84B54A85C7E7830D3A0C9"><span class="codeph"> Novo</span>: O monitor de Tarefa foi criado, mas ainda não aceitou o tarefa. </li>
     <li id="li_76D667D21BDF4FADA6A266A7EB4DC6EE"><span class="codeph"> Processando</span>: O monitor de Tarefa está processando tarefas ativamente. </li>
     <li id="li_3813B2178D7143DEB91804A6C5FF3902"><span class="codeph"> Interrompendo</span>: O monitor de Tarefa está parando um trabalho devido a uma solicitação de parada de trabalho. </li>
     <li id="li_41C2E774FC504B58BD6736119AE9C0AE"><span class="codeph"> Feito</span>: As tarefas atribuídas aos trabalhos do monitor de tarefa foram concluídas. </li>
     <li id="li_EB2322BB11314B97998D467F4620ED2E"><span class="codeph"> Falha</span>: Indica um erro fatal. </li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

