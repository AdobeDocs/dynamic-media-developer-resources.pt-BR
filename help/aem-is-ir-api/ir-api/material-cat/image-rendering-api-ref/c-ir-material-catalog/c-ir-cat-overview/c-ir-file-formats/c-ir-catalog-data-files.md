---
description: Os arquivos de dados do catálogo podem ter qualquer nome e sufixo de arquivo (exceto .ini).
seo-description: Os arquivos de dados do catálogo podem ter qualquer nome e sufixo de arquivo (exceto .ini).
seo-title: Arquivos de dados do catálogo
solution: Experience Manager
title: Arquivos de dados do catálogo
uuid: 33d991d6-5aa7-4cc6-88d4-10c4bb83d786
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---


# Arquivos de dados de catálogo{#catalog-data-files}

Os arquivos de dados do catálogo podem ter qualquer nome e sufixo de arquivo (exceto .ini).

Os arquivos de dados de catálogo podem ser mantidos prontamente usando aplicativos que suportam arquivos de dados de texto delimitados por tabulação, como Microsoft Excel e Access.

Essencialmente uma tabela bidimensional, um arquivo de dados de catálogo consiste em um registro de cabeçalho que identifica as colunas de dados e qualquer número de registros de dados (linhas). Os campos nos registros de cabeçalho e dados são separados por caracteres `<TAB>` únicos. Os registros são separados por um único `<CR>` (código ASCII 0xD), um único `<LF>` (código ASCII 0xA) ou um par `<CR><LF>`.

O registro de cabeçalho deve conter os nomes exatos de cada campo de dados. Campos vazios não são permitidos na linha de cabeçalho. Os nomes de campos de dados não fazem distinção entre maiúsculas e minúsculas. Todos os nomes de campo devem ser exclusivos.

Não é permitido nenhum espaço em branco diferente dos separadores de campo `<TAB>` nos registros de cabeçalho e dados.

Nos registros de dados, dois caracteres adjacentes `<TAB>` indicam um campo vazio. Campos vazios herdarão valores padrão dos atributos do catálogo ou dos padrões do servidor.

Os campos de dados não devem conter caracteres `<CR>`, `<LF>` ou `<TAB>`, a menos que o valor de dados seja do tipo texto e seja inserido por aspas simples ou duplas. Os campos de dados não devem ser codificados por HTTP.

Vários valores de dados no mesmo campo são separados por vírgulas (&#39;,&#39;), salvo indicação em contrário.

Colunas cujos nomes começam com &#39;.&#39; sejam ignoradas; isso permite armazenar dados em catálogos de materiais que não interessam à renderização de imagens. As colunas com nomes de cabeçalho desconhecidos são ignoradas e um aviso é gravado no arquivo de log.

Os nomes de campo podem consistir em qualquer combinação de letras, números ASCII, bem como &quot;-&quot; e &quot;_&quot;.

Uma ou mais colunas podem ser usadas como chaves de índice. Se a mesma chave ocorrer mais de uma vez no mesmo arquivo de dados, a instância posterior prevalecerá.
