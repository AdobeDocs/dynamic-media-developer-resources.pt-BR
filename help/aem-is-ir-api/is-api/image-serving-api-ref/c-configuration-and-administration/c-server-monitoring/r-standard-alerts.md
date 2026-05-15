---
description: Os alertas padrão são enviados com uma mensagem de email consolidada ao final do intervalo de média configurado.
solution: Experience Manager
title: Alertas padrão
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: eb691988-9f03-463f-bed5-2c230431f537
TQID: 'https://experienceleague.adobe.com/EJzmjshgrIk8hpvZvljpsWTHSI-mG67UNAg2NVjBcZg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 222
ht-degree: 0%

---

# Alertas padrão{#standard-alerts}

Os alertas padrão são enviados com uma mensagem de email consolidada ao final do intervalo de média configurado.

A tabela a seguir descreve cada tipo de alerta padrão.

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Tipo de Alerta</b> </th> 
   <th class="entry"> <b>Id do Título</b> </th> 
   <th class="entry"> <b>Descrição</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Solicitação bloqueada </p> </td> 
   <td> <p>Bloquear </p> </td> 
   <td> <p>Enviado quando uma solicitação não retorna uma resposta ao cliente dentro do limite especificado. Pode ser um indicativo de solicitações travadas, o que pode causar o esgotamento do pool de threads Java. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Alta simultaneidade </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> Emitido quando o número de solicitações processadas simultaneamente (a <i>sobreposição</i>) excede o limite especificado. Pode indicar uma condição de sobrecarga do servidor. </td> 
  </tr> 
  <tr> 
   <td> <p>Tráfego mínimo </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>Gerado quando a taxa de solicitação geral cai abaixo do limite especificado. Normalmente indica um problema de comunicação do servidor (por exemplo, quando um servidor é colocado offline). </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Taxa de erro </p> </td> 
   <td> <p>Erro </p> </td> 
   <td> <p>Emitido quando a taxa média de respostas de erro HTTP durante o intervalo de amostragem excede o limite especificado. Pode indicar problemas de configuração, imagens ausentes ou erros de programação ou banco de dados do site. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Tempo de resposta </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>Enviado quando o tempo médio de processamento de solicitações durante o intervalo de amostragem ultrapassa o limite especificado. Normalmente indica uma condição de sobrecarga temporária ou persistente do servidor ou do sistema de armazenamento de imagens de back-end. </p> <p>Respostas de erro não são consideradas ao calcular o tempo médio de resposta. </p> </td> 
  </tr> 
 </tbody> 
</table>
