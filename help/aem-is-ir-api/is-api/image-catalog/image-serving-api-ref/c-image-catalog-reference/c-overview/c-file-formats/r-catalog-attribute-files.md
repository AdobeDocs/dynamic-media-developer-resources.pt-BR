---
description: Os arquivos de atributos de catálogo podem ter qualquer nome, mas devem ter um sufixo de arquivo .ini. Elas podem ser prontamente mantidas usando qualquer editor de texto.
solution: Experience Manager
title: Arquivos de atributo de catálogo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
TQID: 'https://experienceleague.adobe.com/RCxeXg3wb10jo37biAs1puqmEo8bAL-i-oZBwGHuloA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 195
ht-degree: 0%

---

# Arquivos de atributo de catálogo{#catalog-attribute-files}

Os arquivos de atributos de catálogo podem ter qualquer nome, mas devem ter um sufixo de arquivo .ini. Elas podem ser prontamente mantidas usando qualquer editor de texto.

Os arquivos de atributo de catálogo consistem em um conjunto de registros de texto, separados por um único `<CR>` (código ASCII `0xD`), um único `<LF>` (código ASCII `0xA`) ou um par `<CR><LF>`. Cada registro consiste em um nome de atributo e um ou mais valores de atributo separados por vírgulas:

`*`nome`*= *`valores`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> valores</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> values</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nome</span> </p> </td> 
  <td class="stentry"> <p>Nome do atributo. Pode consistir em uma ou mais letras, número, - e _. Não diferencia maiúsculas de minúsculas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Valor do atributo. Não deve incluir <span class="codeph"> &lt;CR&gt;</span> ou <span class="codeph"> &lt;LF&gt;</span> caracteres, a menos que seja evitado por uma única barra invertida logo antes do caractere de nova linha. </p></td> 
 </tr> 
</table>

O espaço em branco entre os tokens é opcional.

Registros com nomes de atributo desconhecidos são ignorados pelo [!DNL Platform Server].

Os nomes de atributos podem consistir em qualquer combinação de letras ASCII, números, bem como &quot;-&quot;, &quot;_&quot; e &quot;.&quot;.

Se o mesmo nome de atributo ocorrer mais de uma vez no mesmo arquivo de atributo, o último encontrado prevalecerá.

Use # como o primeiro caractere para marcar qualquer registro como um comentário, que o analisador ignora.
