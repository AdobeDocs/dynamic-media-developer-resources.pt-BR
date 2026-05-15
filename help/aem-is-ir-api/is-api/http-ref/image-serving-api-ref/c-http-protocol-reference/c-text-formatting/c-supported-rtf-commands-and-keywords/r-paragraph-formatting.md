---
description: Os seguintes comandos de formatação de parágrafo são compatíveis.
solution: Experience Manager
title: Formatação de parágrafo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a2235082-714c-4ae3-ae06-c91ea2fb5abb
TQID: 'https://experienceleague.adobe.com/bksi7t36irm8XQqI0LtJl3kNaSCZANRzbCKf80o-eNM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 0%

---

# Formatação de parágrafo{#paragraph-formatting}

Os seguintes comandos de formatação de parágrafo são compatíveis.

<table id="table_5DD044E1C0614A29A2413557DF57197D"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Comando </p> </th> 
   <th class="entry"> <p>Descrição </p> </th> 
   <th class="entry"> <p>Notas </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <span class="codeph"> \pard </span> </td> 
   <td> <p>Redefinir a formatação de parágrafo para o padrão. </p> </td> 
   <td> <p> <span class="codeph"> somente textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql </span> </td> 
   <td> <p>Texto alinhado à esquerda. </p> </td> 
   <td> <p>Padrão. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr </span> </td> 
   <td> <p>Texto alinhado à direita. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc </span> </td> 
   <td> <p>Centralizar texto horizontalmente. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj </span> </td> 
   <td> <p>Justificar o texto horizontalmente. </p> </td> 
   <td> <p> <span class="codeph"> somente textPs= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql </span> </td> 
   <td> <p>Alinhar à esquerda a última linha de um parágrafo. </p> </td> 
   <td> <p>Padrão; <span class="codeph"> textPs= </span> somente; ignorado se <span class="codeph"> \qj </span> não estiver ativo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr </span> </td> 
   <td> <p>Alinhar à direita a última linha de um parágrafo justificado. </p> </td> 
   <td> <p> <span class="codeph"> textPs= somente </span>; ignorado se <span class="codeph"> \qj </span> não estiver ativo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc </span> </td> 
   <td> <p>Centralizar a última linha de um parágrafo justificado. </p> </td> 
   <td> <p> <span class="codeph"> textPs= somente </span>; ignorado se <span class="codeph"> \qj </span> não estiver ativo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj </span> </td> 
   <td> <p>Justificar (alongar) a última linha de um parágrafo justificado. </p> </td> 
   <td> <p> <span class="codeph"> textPs= somente </span>; ignorado se <span class="codeph"> \qj </span> não estiver ativo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi <span class="varname"> N </span> </span> </td> 
   <td> <p>Recuo da primeira linha. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> somente. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li <span class="varname"> N </span> </span> </td> 
   <td> <p>Recuo à esquerda. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> somente. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri <span class="varname"> N </span> </span> </td> 
   <td> <p>Recuo à direita. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> somente. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl <span class="varname"> N </span> </span> </td> 
   <td> <p>Espaço entre linhas. </p> </td> 
   <td> <p>0 (padrão) para espaçamento automático de linha; valores positivos para usar somente o valor se maior que o espaçamento padrão de linha; valor negativo para forçar o espaçamento. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult <span class="varname"> N </span> </span> </td> 
   <td> <p>Sinalizador múltiplo de espaçamento entre linhas. </p> </td> 
   <td> <p>Defina como 0 (padrão) se <span class="codeph"> \sl </span> estiver em twips, como 1 se <span class="codeph"> \sl </span> estiver em múltiplos do espaçamento padrão. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb <span class="varname"> N </span> </span> </td> 
   <td> <p>Espaço extra antes do parágrafo. </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span> aplica <span class="codeph"> \sb </span> ao primeiro parágrafo na caixa de texto, <span class="codeph"> textPs= </span> não aplica. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa <span class="varname"> N </span> </span> </td> 
   <td> <p>Espaço extra após o parágrafo. </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span> aplica <span class="codeph"> \sa </span> ao último parágrafo da caixa de texto, <span class="codeph"> textPs= </span> não aplica. </p> </td> 
  </tr> 
 </tbody> 
</table>
