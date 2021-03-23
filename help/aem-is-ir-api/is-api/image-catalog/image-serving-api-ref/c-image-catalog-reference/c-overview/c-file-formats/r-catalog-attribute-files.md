---
description: Os arquivos de atributos do catálogo podem ter qualquer nome, mas devem ter um sufixo de arquivo .ini. Eles podem ser prontamente mantidos usando qualquer editor de texto.
seo-description: Os arquivos de atributos do catálogo podem ter qualquer nome, mas devem ter um sufixo de arquivo .ini. Eles podem ser prontamente mantidos usando qualquer editor de texto.
seo-title: Arquivos de atributo do catálogo
solution: Experience Manager
title: Arquivos de atributo do catálogo
uuid: 63985780-f032-4542-8d84-b8b608ceea4b
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# Arquivos de atributo do catálogo{#catalog-attribute-files}

Os arquivos de atributos do catálogo podem ter qualquer nome, mas devem ter um sufixo de arquivo .ini. Eles podem ser prontamente mantidos usando qualquer editor de texto.

Os arquivos de atributos do catálogo consistem em um conjunto de registros de texto, separados por um único `<CR>` (código ASCII `0xD`), um único `<LF>` (código ASCII `0xA`) ou um par `<CR><LF>`. Cada registro consiste em um nome de atributo e um ou mais valores de atributo separados por vírgula:

`*``*= *`valores de nomes`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> values</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> valores</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p> </td> 
  <td class="stentry"> <p>Nome do atributo. Pode consistir em uma ou mais letras, número, - e _. Não diferencia maiúsculas de minúsculas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Valor do atributo. Não deve incluir caracteres <span class="codeph"> &lt;CR&gt;</span> ou <span class="codeph"> &lt;LF&gt;</span>, a menos que sejam evitados por uma única barra invertida antes do caractere de nova linha. </p></td> 
 </tr> 
</table>

O espaço em branco entre tokens é opcional.

Os registros com nomes de atributos desconhecidos são ignorados pelo Servidor de Plataforma.

Os nomes de atributos podem consistir em qualquer combinação de letras, números ASCII, assim como &quot;-&quot;, &quot;_&quot; e &quot;.&quot;.

Se o mesmo nome de atributo ocorrer mais de uma vez no mesmo arquivo de atributo, prevalecerá o último encontrado.

Use # como o primeiro caractere para marcar qualquer registro como um comentário, que o analisador ignora.
