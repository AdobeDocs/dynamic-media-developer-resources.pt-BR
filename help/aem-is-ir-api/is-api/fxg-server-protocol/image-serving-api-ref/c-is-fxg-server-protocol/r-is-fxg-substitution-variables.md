---
description: As variáveis de substituição são usadas para transferir valores do URL de solicitação para modelos FXG armazenados no servidor.
seo-description: As variáveis de substituição são usadas para transferir valores do URL de solicitação para modelos FXG armazenados no servidor.
seo-title: Variáveis de substituição
solution: Experience Manager
title: Variáveis de substituição
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 87cd9594-ba3b-429d-aa57-399902ef3abe
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---


# Variáveis de substituição{#substitution-variables}

As variáveis de substituição são usadas para transferir valores do URL de solicitação para modelos FXG armazenados no servidor.

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

* Definições e referências de variáveis podem ocorrer na parte do query do URL da solicitação.
* As variáveis são definidas como acima, semelhantes a outros comandos IS; o &#39;$&#39; à esquerda identifica o comando como uma definição de variável.
* O nome da variável `*`var`*` faz distinção entre maiúsculas e minúsculas e pode consistir em qualquer combinação de letras, números, &#39;-&#39; e &#39;_&#39;.
* O valor importante deve ser codificado em URL de passagem única para transmissão segura HTTP.

