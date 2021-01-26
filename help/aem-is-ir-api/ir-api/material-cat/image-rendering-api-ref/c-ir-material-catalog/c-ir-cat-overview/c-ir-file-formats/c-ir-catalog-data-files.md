---
description: Os arquivos de dados do catálogo podem ter qualquer nome e sufixo de arquivo (exceto .ini).
seo-description: Os arquivos de dados do catálogo podem ter qualquer nome e sufixo de arquivo (exceto .ini).
seo-title: Arquivos de dados do catálogo
solution: Experience Manager
title: Arquivos de dados do catálogo
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 33d991d6-5aa7-4cc6-88d4-10c4bb83d786
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---


# Arquivos de dados do catálogo{#catalog-data-files}

Os arquivos de dados do catálogo podem ter qualquer nome e sufixo de arquivo (exceto .ini).

Os arquivos de dados do catálogo podem ser mantidos prontamente usando aplicativos que suportam arquivos de dados de texto delimitados por tabulação, como o Microsoft Excel e o Access.

Essencialmente uma tabela bidimensional, um arquivo de dados de catálogo consiste em um registro de cabeçalho que identifica as colunas de dados e qualquer número de registros de dados (linhas). Os campos nos registros de cabeçalho e de dados são separados por caracteres `<TAB>` únicos. Os registros são separados por um único par `<CR>` (código ASCII 0xD), um único par `<LF>` (código ASCII 0xA) ou um par `<CR><LF>`.

O registro de cabeçalho deve conter os nomes exatos de cada campo de dados. Campos vazios não são permitidos na linha de cabeçalho. Os nomes de campos de dados não distinguem maiúsculas de minúsculas. Todos os nomes de campo devem ser exclusivos.

Nenhum espaço em branco além dos separadores de campo `<TAB>` é permitido nos registros de cabeçalho e dados.

Nos registros de dados, dois caracteres adjacentes `<TAB>` indicam um campo vazio. Campos vazios herdarão valores padrão dos atributos do catálogo ou dos padrões do servidor.

Os campos de dados não devem conter caracteres `<CR>`, `<LF>` ou `<TAB>`, a menos que o valor de dados seja do tipo texto e esteja entre aspas simples ou duplos. Os campos de dados não devem ser codificados por HTTP.

Vários valores de dados no mesmo campo são separados por vírgulas (&#39;,&#39;), salvo indicação em contrário.

Colunas cujos nomes são start com &#39;.&#39; sejam ignorados; isso permite armazenar dados em catálogos de materiais que não interessam à renderização de imagens. As colunas com nomes de cabeçalho desconhecidos são ignoradas e um aviso é gravado no arquivo de log.

Os nomes de campo podem consistir em qualquer combinação de letras ASCII, números, bem como &quot;-&quot; e &quot;_&quot;.

Uma ou mais colunas podem ser usadas como chaves de índice. Se a mesma chave ocorrer mais de uma vez no mesmo arquivo de dados, a instância posterior prevalecerá.
