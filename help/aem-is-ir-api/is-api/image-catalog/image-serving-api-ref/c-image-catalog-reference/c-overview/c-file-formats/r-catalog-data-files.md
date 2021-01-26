---
description: Os arquivos de dados do catálogo podem ter qualquer nome e sufixo de arquivo (exceto .ini). Eles podem ser mantidos prontamente usando aplicativos que suportam arquivos de dados de texto delimitados por tabulação, como o Microsoft Excel e o Access.
seo-description: Os arquivos de dados do catálogo podem ter qualquer nome e sufixo de arquivo (exceto .ini). Eles podem ser mantidos prontamente usando aplicativos que suportam arquivos de dados de texto delimitados por tabulação, como o Microsoft Excel e o Access.
seo-title: Arquivos de dados do catálogo
solution: Experience Manager
title: Arquivos de dados do catálogo
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 0f66e2fe-5b8a-43d3-bf2e-8dd79da6a581
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---


# Arquivos de dados do catálogo{#catalog-data-files}

Os arquivos de dados do catálogo podem ter qualquer nome e sufixo de arquivo (exceto .ini). Eles podem ser mantidos prontamente usando aplicativos que suportam arquivos de dados de texto delimitados por tabulação, como o Microsoft Excel e o Access.

Essencialmente uma tabela bidimensional, um arquivo de dados de catálogo consiste em um registro de cabeçalho que identifica as colunas de dados e qualquer número de registros de dados (linhas). Os campos nos registros de cabeçalho e de dados são separados por caracteres `<TAB>` únicos. Os registros são separados por um único `<CR>` (código ASCII `0xD`), um único `<LF>` (código ASCII `0xA`) ou um par `<CR><LF>`.

O registro de cabeçalho deve conter os nomes exatos de cada campo de dados. Campos vazios não são permitidos na linha de cabeçalho. Os nomes de campos de dados não distinguem maiúsculas de minúsculas. Todos os nomes de campo devem ser exclusivos.

Caracteres de espaço não podem ser usados como separadores de campo. Não são permitidos espaços no registro de cabeçalho. Nos registros de dados, quaisquer espaços no início ou no fim de um campo de dados são considerados parte desse campo de dados.

Nos registros de dados, dois caracteres adjacentes `<TAB>` indicam um campo vazio. Campos vazios podem herdar valores padrão dos atributos do catálogo ou dos padrões do servidor.

Como opção, os campos de dados podem ser delimitados por aspas de duplo. Eles não devem conter caracteres `<CR>`, `<LF>` ou `<TAB>`, a menos que o valor de dados seja do tipo texto e esteja entre aspas de duplo. Os campos de dados não devem ser codificados por HTTP.

Vários valores de dados no mesmo campo são separados por vírgulas, salvo indicação em contrário.

Colunas cujos nomes são start com &quot;.&quot; são ignorados. Isso permite armazenar dados em catálogos de imagens, o que não interessa ao Serviço de imagens. As colunas com nomes de cabeçalho desconhecidos são ignoradas e um aviso é gravado no arquivo de log.

Os nomes de campo podem consistir em qualquer combinação de letras ASCII, números, bem como &quot;-&quot; e &quot;_&quot;.

Uma ou mais colunas podem ser usadas como chaves de índice. Se a mesma chave ocorrer mais de uma vez no mesmo arquivo de dados, a instância posterior prevalecerá.
