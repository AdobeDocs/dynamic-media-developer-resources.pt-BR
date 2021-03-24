---
description: Os arquivos de dados do catálogo podem ter qualquer nome e sufixo de arquivo (exceto .ini). Eles podem ser mantidos prontamente usando aplicativos que suportam arquivos de dados de texto delimitados por tabulação, como Microsoft Excel e Access.
solution: Experience Manager
title: Arquivos de dados do catálogo
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---


# Arquivos de dados de catálogo{#catalog-data-files}

Os arquivos de dados do catálogo podem ter qualquer nome e sufixo de arquivo (exceto .ini). Eles podem ser mantidos prontamente usando aplicativos que suportam arquivos de dados de texto delimitados por tabulação, como Microsoft Excel e Access.

Essencialmente uma tabela bidimensional, um arquivo de dados de catálogo consiste em um registro de cabeçalho que identifica as colunas de dados e qualquer número de registros de dados (linhas). Os campos nos registros de cabeçalho e dados são separados por caracteres `<TAB>` únicos. Os registros são separados por um único `<CR>` (código ASCII `0xD`), um único `<LF>` (código ASCII `0xA`) ou um par `<CR><LF>`.

O registro de cabeçalho deve conter os nomes exatos de cada campo de dados. Campos vazios não são permitidos na linha de cabeçalho. Os nomes de campos de dados não fazem distinção entre maiúsculas e minúsculas. Todos os nomes de campo devem ser exclusivos.

Caracteres de espaço não podem ser usados como separadores de campo. Não são permitidos espaços no registro de cabeçalho. Em registros de dados, quaisquer espaços no início ou no fim de um campo de dados são considerados parte desse campo de dados.

Nos registros de dados, dois caracteres adjacentes `<TAB>` indicam um campo vazio. Campos vazios podem herdar valores padrão dos atributos do catálogo ou dos padrões do servidor.

Como opção, os campos de dados podem ser colocados por aspas duplas. Eles não devem conter caracteres `<CR>`, `<LF>` ou `<TAB>`, a menos que o valor de dados seja do tipo texto e seja inserido por aspas duplas. Os campos de dados não devem ser codificados por HTTP.

Vários valores de dados no mesmo campo são separados por vírgulas, salvo indicação em contrário.

Colunas cujos nomes começam com &quot;.&quot; são ignoradas. Isso permite armazenar dados em catálogos de imagens, o que não interessa ao Serviço de imagens. As colunas com nomes de cabeçalho desconhecidos são ignoradas e um aviso é gravado no arquivo de log.

Os nomes de campo podem consistir em qualquer combinação de letras, números ASCII, bem como &quot;-&quot; e &quot;_&quot;.

Uma ou mais colunas podem ser usadas como chaves de índice. Se a mesma chave ocorrer mais de uma vez no mesmo arquivo de dados, a instância posterior prevalecerá.
