---
title: Arquivos de atributo de catálogo
description: Os arquivos de atributos de catálogo podem ter qualquer nome, mas devem ter um sufixo de arquivo .ini. Elas podem ser prontamente mantidas usando qualquer editor de texto.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
TQID: 'https://experienceleague.adobe.com/OwtzX3xKh5ByC3eUhz7dmFjGR5HRD9cbE6atUEL0Nic'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 192
ht-degree: 0%

---

# Arquivos de atributo de catálogo{#catalog-attribute-files}

Os arquivos de atributos de catálogo podem ter qualquer nome, mas devem ter um sufixo de arquivo `.ini`. Elas podem ser prontamente mantidas usando qualquer editor de texto.

Os arquivos de atributo de catálogo consistem em um conjunto de registros de texto, separados por um único `<CR>` (código ASCII 0xD), um único `<LF>` (código ASCII 0xA) ou um par `<CR><LF>`. Cada registro consiste em um nome de atributo e um ou mais valores de atributo separados por vírgulas:

`*`nome`*= *`valor`*&#42;[, *`valor`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> nome </span> </span> </p> </td> 
  <td class="stentry"> <p>Nome do atributo; pode consistir em uma ou mais letras, número, - (hífen) e _ (sublinhado); não diferencia maiúsculas de minúsculas.</p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> valor </span> </span> </p> </td> 
  <td class="stentry"> <p>O valor do atributo; não deve incluir <span class="codeph"> &lt;CR&gt; </span> ou <span class="codeph"> &lt;LF&gt; </span> caracteres, a menos que seja evitado por uma única barra invertida logo antes do caractere de nova linha. </p> </td> 
 </tr> 
</table>

* O espaço em branco entre os tokens é opcional.
* O [!DNL Platform Server] ignora registros com nomes de atributo desconhecidos.
* Os nomes de atributos podem consistir em qualquer combinação de letras ASCII, números e `-`, `_` e `.` caracteres.
* Se o mesmo nome de atributo ocorrer mais de uma vez no mesmo arquivo de atributo, o último encontrado prevalecerá.
* Use `#` como o primeiro caractere para marcar qualquer registro como um comentário que o analisador ignora.

