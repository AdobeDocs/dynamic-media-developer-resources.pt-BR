---
description: Os arquivos de atributo do catálogo podem ter qualquer nome, mas devem ter um sufixo de arquivo .ini. Eles podem ser prontamente mantidos usando qualquer editor de texto.
seo-description: Os arquivos de atributo do catálogo podem ter qualquer nome, mas devem ter um sufixo de arquivo .ini. Eles podem ser prontamente mantidos usando qualquer editor de texto.
seo-title: Arquivos de atributo do catálogo
solution: Experience Manager
title: Arquivos de atributo do catálogo
topic: Scene7 Image Serving - Image Rendering API
uuid: ea2bddad-2c4a-43c1-9b62-6e724fcfb8a0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Arquivos de atributo do catálogo{#catalog-attribute-files}

Os arquivos de atributo do catálogo podem ter qualquer nome, mas devem ter um sufixo de arquivo .ini. Eles podem ser prontamente mantidos usando qualquer editor de texto.

Os arquivos de atributos do catálogo consistem em um conjunto de registros de texto, separados por um único `<CR>` (código ASCII 0xD), um único `<LF>` (código ASCII 0xA) ou um `<CR><LF>` par. Cada registro consiste em um nome de atributo e um ou mais valores de atributo separados por vírgula:

` *``*= *``*&#42;[, *`namassessment evalue`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> nome </span></span> </p> </td> 
  <td class="stentry"> <p>Nome do atributo; pode consistir em uma ou mais letras, número, '-' e '_'; não diferencia maiúsculas de minúsculas. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> valor </span></span> </p> </td> 
  <td class="stentry"> <p>Valor do atributo; não deve incluir caracteres <span class="codeph"> &lt;CR&gt; </span>ou <span class="codeph"> &lt;LF&gt; </span> , a menos que sejam escapados por uma única barra invertida antes do caractere de nova linha. </p> </td> 
 </tr> 
</table>

* O espaço em branco entre tokens é opcional.
* Os registros com nomes de atributos desconhecidos são ignorados pelo Servidor de Plataformas.
* Os nomes de atributos podem consistir em qualquer combinação de letras, números ASCII, bem como &quot;-&quot;, &quot;_&quot; e &quot;.&quot;
* Se o mesmo nome de atributo ocorrer mais de uma vez no mesmo arquivo de atributo, o último encontrado prevalecerá.
* Use &#39;#&#39; como o primeiro caractere para marcar qualquer registro como um comentário que o analisador ignora.

