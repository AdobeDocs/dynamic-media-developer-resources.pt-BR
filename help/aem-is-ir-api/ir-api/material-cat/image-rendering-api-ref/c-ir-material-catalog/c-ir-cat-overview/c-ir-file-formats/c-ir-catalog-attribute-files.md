---
title: Arquivos de atributo de catálogo
description: Os arquivos de atributos de catálogo podem ter qualquer nome, mas devem ter um sufixo de arquivo .ini. Elas podem ser prontamente mantidas usando qualquer editor de texto.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---

# Arquivos de atributo de catálogo{#catalog-attribute-files}

Os arquivos de atributo de catálogo podem ter qualquer nome, mas devem ter um `.ini` sufixo do arquivo. Elas podem ser prontamente mantidas usando qualquer editor de texto.

Os arquivos de atributo de catálogo consistem em um conjunto de registros de texto, separados por um único `<CR>` (código ASCII 0xD), um único `<LF>` (código ASCII 0xA) ou um `<CR><LF>` emparelhar. Cada registro consiste em um nome de atributo e um ou mais valores de atributo separados por vírgulas:

`*`name`*= *`value`*&#42;[, *`value`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
  <td class="stentry"> <p>Nome do atributo; pode consistir em uma ou mais letras, número, '-' e '_'; não diferencia maiúsculas de minúsculas. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor de atributo; não deve incluir <span class="codeph"> &lt;cr&gt; </span>ou <span class="codeph"> &lt;lf&gt; </span> caracteres, a menos que sejam evitados por uma única barra invertida logo antes do caractere de nova linha. </p> </td> 
 </tr> 
</table>

* O espaço em branco entre os tokens é opcional.
* Registros com nomes de atributo desconhecidos são ignorados pelo [!DNL Platform Server].
* Os nomes de atributos podem consistir em qualquer combinação de letras ASCII, números e &quot;-&quot;, &quot;_&quot; e &quot;.&quot;
* Se o mesmo nome de atributo ocorrer mais de uma vez no mesmo arquivo de atributo, o último encontrado prevalecerá.
* Use &#39;#&#39; como o primeiro caractere para marcar qualquer registro como um comentário que o analisador ignora.
