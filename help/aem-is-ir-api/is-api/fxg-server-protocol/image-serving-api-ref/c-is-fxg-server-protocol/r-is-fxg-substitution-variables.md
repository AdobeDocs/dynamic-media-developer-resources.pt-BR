---
description: A variável de substituição é usada para transferir valores do URL da solicitação para modelos FXG armazenados no servidor.
solution: Experience Manager
title: Variáveis de substituição
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 539d8863-e94d-45dc-bb8c-3db7bead0051
TQID: 'https://experienceleague.adobe.com/-IHIbaXxoDEGqbV2inp4RlmWpH-8js7Dn9b-CK1paxg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 117
ht-degree: 0%

---

# Variáveis de substituição{#substitution-variables}

A variável de substituição é usada para transferir valores do URL da solicitação para modelos FXG armazenados no servidor.

` $ *`var`*= *`value`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Nome da variável. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> valor </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor com o qual a variável deve ser definida (string). </p> </td> 
 </tr> 
</table>

* Definições e referências de variáveis podem ocorrer na parte de consulta do URL da solicitação.
* As variáveis são definidas como acima, de modo semelhante a outros comandos IS; o &#39;$&#39; à esquerda identifica o comando como uma definição de variável.
* O nome da variável `*`var`*` diferencia maiúsculas de minúsculas e pode consistir em qualquer combinação de letras, números, &#39;-&#39; e &#39;_&#39;.
* O valor importante deve ser codificado em URL de passagem única para transmissão HTTP segura.
