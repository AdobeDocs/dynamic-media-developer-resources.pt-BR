---
description: Os arquivos de atributos do catálogo podem ter qualquer nome, mas devem ter um sufixo de arquivo .ini. Eles podem ser prontamente mantidos usando qualquer editor de texto.
solution: Experience Manager
title: Arquivos de atributo do catálogo
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '202'
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
