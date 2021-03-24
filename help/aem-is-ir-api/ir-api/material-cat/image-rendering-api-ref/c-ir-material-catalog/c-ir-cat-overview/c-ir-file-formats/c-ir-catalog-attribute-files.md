---
description: Os arquivos de atributos do catálogo podem ter qualquer nome, mas devem ter um sufixo de arquivo .ini. Eles podem ser prontamente mantidos usando qualquer editor de texto.
solution: Experience Manager
title: Arquivos de atributo do catálogo
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 0%

---


# Arquivos de atributo do catálogo{#catalog-attribute-files}

Os arquivos de atributos do catálogo podem ter qualquer nome, mas devem ter um sufixo de arquivo .ini. Eles podem ser prontamente mantidos usando qualquer editor de texto.

Os arquivos de atributos do catálogo consistem em um conjunto de registros de texto, separados por um único `<CR>` (código ASCII 0xD), um único `<LF>` (código ASCII 0xA) ou um par `<CR><LF>`. Cada registro consiste em um nome de atributo e um ou mais valores de atributo separados por vírgula:

`*``*= *``*&#42;[, *`valor de valor de nome`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
  <td class="stentry"> <p>Nome do atributo; pode consistir em uma ou mais letras, número, '-' e '_'; não diferencia maiúsculas de minúsculas. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor do atributo; não deve incluir <span class="codeph"> &lt;CR&gt; </span> ou <span class="codeph"> &lt;LF&gt; </span> caracteres, a menos que sejam evitados por uma única barra invertida antes do caractere de nova linha. </p> </td> 
 </tr> 
</table>

* O espaço em branco entre tokens é opcional.
* Os registros com nomes de atributos desconhecidos são ignorados pelo Servidor de Plataforma.
* Os nomes de atributos podem consistir em qualquer combinação de letras, números ASCII, assim como &quot;-&quot;, &quot;_&quot; e &quot;.&quot;
* Se o mesmo nome de atributo ocorrer mais de uma vez no mesmo arquivo de atributo, prevalecerá o último encontrado.
* Use &#39;#&#39; como o primeiro caractere para marcar qualquer registro como um comentário que o analisador ignora.

