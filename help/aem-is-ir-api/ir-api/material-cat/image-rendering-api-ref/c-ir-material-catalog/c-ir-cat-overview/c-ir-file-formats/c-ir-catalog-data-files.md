---
title: Arquivos de dados do catálogo
description: Os arquivos de dados do catálogo podem ter qualquer nome e sufixo de arquivo (exceto .ini).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1fb91795-f699-40b4-a6bc-6eab3e1ecd1d
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Arquivos de dados do catálogo{#catalog-data-files}

Os arquivos de dados do catálogo podem ter qualquer nome e sufixo de arquivo (exceto `.ini`).

Os arquivos de dados de catálogo podem ser mantidos prontamente usando aplicativos que suportam arquivos de dados de texto delimitados por tabulação, como Microsoft® Excel e Access.

Essencialmente uma tabela bidimensional, um arquivo de dados de catálogo consiste em um registro de cabeçalho que identifica as colunas de dados e qualquer número de registros de dados (linhas). Os campos no cabeçalho e nos registros de dados são separados por `<TAB>` caracteres. Os registros são separados por um único `<CR>` (Código ASCII `0xD`), um único `<LF>` (Código ASCII `0xA`), ou uma `<CR><LF>` par.

O registro de cabeçalho deve conter os nomes exatos de cada campo de dados. Campos vazios não são permitidos na linha de cabeçalho. Os nomes de campos de dados não fazem distinção entre maiúsculas e minúsculas. Todos os nomes de campo devem ser exclusivos.

Nenhum espaço em branco diferente do `<TAB>` separadores de campo são permitidos em registros de cabeçalho e dados.

Nos registros de dados, dois `<TAB>` caracteres indicam um campo vazio. Campos vazios herdam valores padrão dos atributos do catálogo ou dos padrões do servidor.

Os campos de dados não devem conter `<CR>`, `<LF>`ou `<TAB>` caracteres, a menos que o valor de dados seja do tipo texto e seja inserido por aspas simples ou duplas. Não codifique campos de dados por HTTP.

Vários valores de dados no mesmo campo são separados por vírgulas (&#39;,&#39;), salvo indicação em contrário.

Colunas cujos nomes começam com &#39;.&#39; sejam ignoradas; isso permite armazenar dados em catálogos de materiais que não interessam à renderização de imagens. As colunas com nomes de cabeçalho desconhecidos são ignoradas e um aviso é gravado no arquivo de log.

Os nomes de campo podem consistir em qualquer combinação de letras ASCII, números e &quot;-&quot; e &quot;_&quot;.

Uma ou mais colunas podem ser usadas como chaves de índice. Se a mesma chave ocorrer mais de uma vez no mesmo arquivo de dados, a instância posterior prevalecerá.
