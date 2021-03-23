---
description: Os alertas padrão são enviados com uma mensagem de email consolidada no final do intervalo de média configurado.
seo-description: Os alertas padrão são enviados com uma mensagem de email consolidada no final do intervalo de média configurado.
seo-title: Alertas padrão
solution: Experience Manager
title: Alertas padrão
uuid: d3294434-a44b-4742-9d77-a6945760d33c
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---


# Alertas padrão{#standard-alerts}

Os alertas padrão são enviados com uma mensagem de email consolidada no final do intervalo de média configurado.

A tabela a seguir descreve cada tipo de alerta padrão.

<table id="table_02611F1B920E48A6973BFA969CA564EB"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Tipo de alerta</b> </th> 
   <th class="entry"> <b>ID do título</b> </th> 
   <th class="entry"> <b>Descrição</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Solicitação bloqueada </p> </td> 
   <td> <p>Bloquear </p> </td> 
   <td> <p>Enviado quando uma solicitação falha ao retornar uma resposta ao cliente dentro do limite especificado. Pode ser indicativo de solicitações suspensas, o que pode causar a conclusão do conjunto de encadeamentos Java. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Alta simultaneidade </p> </td> 
   <td> <p>Conc </p> </td> 
   <td> Emitido quando o número de solicitações que são processadas simultaneamente (o <i>overlap</i>) excede o limite especificado. Pode ser indicativo de uma condição de sobrecarga do servidor. </td> 
  </tr> 
  <tr> 
   <td> <p>Tráfego mínimo </p> </td> 
   <td> <p>Traf </p> </td> 
   <td> <p>Gerada quando a taxa de solicitação geral cai abaixo do limite especificado. Normalmente indica um problema de comunicação com o servidor (por exemplo, quando um servidor é retirado da linha). </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Taxa de erro </p> </td> 
   <td> <p>Erro </p> </td> 
   <td> <p>Emitido quando a taxa média de respostas de erro HTTP durante o intervalo de amostragem excede o limite especificado. Pode ser indicativo de problemas de configuração, imagens ausentes, programação de site ou erros de banco de dados. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Tempo de resposta </p> </td> 
   <td> <p>RTime </p> </td> 
   <td> <p>Enviado quando o tempo médio de processamento da solicitação durante o intervalo de amostragem aumenta acima do limite especificado. Normalmente indica uma condição de sobrecarga temporária ou persistente do servidor ou do sistema de armazenamento de imagem de back-end. </p> <p>As respostas de erro não são consideradas ao calcular o tempo médio de resposta. </p> </td> 
  </tr> 
 </tbody> 
</table>

