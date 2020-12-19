---
description: Os seguintes comandos de formatação de parágrafo são suportados.
seo-description: Os seguintes comandos de formatação de parágrafo são suportados.
seo-title: Formatação de parágrafo
solution: Experience Manager
title: Formatação de parágrafo
topic: Scene7 Image Serving - Image Rendering API
uuid: 4f9255b2-3a74-4c9a-80c5-d85b4627027e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Formatação de parágrafo{#paragraph-formatting}

Os seguintes comandos de formatação de parágrafo são suportados.

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
   <td> <span class="codeph"> \pard  </span> </td> 
   <td> <p>Redefina a formatação de parágrafo para o padrão. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> somente </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ql  </span> </td> 
   <td> <p>Alinha o texto à esquerda. </p> </td> 
   <td> <p>Padrão. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qr  </span> </td> 
   <td> <p>Alinha o texto à direita. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qc  </span> </td> 
   <td> <p>Centralizar o texto horizontalmente. </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \qj  </span> </td> 
   <td> <p>Justificar o texto horizontalmente. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> somente </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastql  </span> </td> 
   <td> <p>Alinha a última linha de um parágrafo à esquerda. </p> </td> 
   <td> <p>Padrão; <span class="codeph"> textPs= </span> apenas; ignorado se <span class="codeph"> \qj </span>não está ativo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqr  </span> </td> 
   <td> <p>Alinha à direita a última linha de um parágrafo justificado. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; ignorado se  <span class="codeph"> \qj não  </span> estiver ativo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqc  </span> </td> 
   <td> <p>Centralizar a última linha de um parágrafo justificado. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; ignorado se  <span class="codeph"> \qj não  </span>estiver ativo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \lastqj  </span> </td> 
   <td> <p>Justificar (esticar) a última linha de um parágrafo justificado. </p> </td> 
   <td> <p> <span class="codeph"> textPs=  </span> only; ignorado se  <span class="codeph"> \qj não  </span>estiver ativo. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \fi  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Recuo da primeira linha. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> apenas. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \li  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Recuo à esquerda. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> apenas. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \ri  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Recuo à direita. </p> </td> 
   <td> <p>Twips; <span class="codeph"> textPs= </span> apenas. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sl  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Espaço entre as linhas. </p> </td> 
   <td> <p>0 (padrão) para espaçamento automático de linha; valores positivos para usar apenas valor se maior que o espaçamento padrão entre linhas; valor negativo para forçar o espaçamento. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \slmult  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Espaçamento entre linhas com vários sinalizadores. </p> </td> 
   <td> <p>Defina como 0 (padrão) se <span class="codeph"> \sl </span> estiver em toques, como 1 se <span class="codeph"> \sl </span> estiver em múltiplos do espaçamento padrão. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sb  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Espaço extra antes do parágrafo. </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span>aplica <span class="codeph"> \sb </span> ao primeiro parágrafo na caixa de texto, <span class="codeph"> textPs= </span> não o aplica. </p> </td> 
  </tr> 
  <tr> 
   <td> <span class="codeph"> \sa  <span class="varname"> N  </span> </span> </td> 
   <td> <p>Espaço extra após o parágrafo. </p> </td> 
   <td> <p>Twips; <span class="codeph"> text= </span> aplica <span class="codeph"> \sa </span> ao último parágrafo na caixa de texto, <span class="codeph"> textPs= </span> não o aplica. </p> </td> 
  </tr> 
 </tbody> 
</table>

