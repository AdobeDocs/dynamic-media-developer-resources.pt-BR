---
description: As variáveis de substituição são usadas para transferir valores do URL da solicitação para modelos FXG armazenados no servidor.
solution: Experience Manager
title: Variáveis de substituição
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 539d8863-e94d-45dc-bb8c-3db7bead0051
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---

# Variáveis de substituição{#substitution-variables}

As variáveis de substituição são usadas para transferir valores do URL da solicitação para modelos FXG armazenados no servidor.

` $ *``*= *`varvalue`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Nome da variável. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor ao qual a variável deve ser definida (string). </p> </td> 
 </tr> 
</table>

* Definições e referências de variáveis podem ocorrer na parte de consulta do URL da solicitação.
* As variáveis são definidas como acima, semelhantes a outros comandos IS; o &#39;$&#39; à esquerda identifica o comando como uma definição de variável.
* O nome da variável `*`var`*` diferencia maiúsculas de minúsculas e pode consistir em qualquer combinação de letras, números, &#39;-&#39; e &#39;_&#39;.
* O valor importante deve ser codificado por URL de passagem única para transmissão HTTP segura.
