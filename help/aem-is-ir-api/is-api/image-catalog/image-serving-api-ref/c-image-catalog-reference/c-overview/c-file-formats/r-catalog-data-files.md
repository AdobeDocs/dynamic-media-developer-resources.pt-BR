---
description: Os arquivos de dados do catálogo podem ter qualquer nome e sufixo de arquivo (exceto .ini). Eles podem ser mantidos prontamente usando aplicativos que oferecem suporte a arquivos de dados de texto delimitados por tabulação, como o Microsoft Excel e o Access.
solution: Experience Manager
title: Arquivos de dados do catálogo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4aa20abe-4f84-470b-b5a1-3d9246ab1792
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# Arquivos de dados do catálogo{#catalog-data-files}

Os arquivos de dados do catálogo podem ter qualquer nome e sufixo de arquivo (exceto .ini). Eles podem ser mantidos prontamente usando aplicativos que oferecem suporte a arquivos de dados de texto delimitados por tabulação, como o Microsoft Excel e o Access.

Essencialmente uma tabela bidimensional, um arquivo de dados de catálogo consiste em um registro de cabeçalho que identifica as colunas de dados e qualquer número de registros de dados (linhas). Os campos no cabeçalho e nos registros de dados são separados por `<TAB>` caracteres. Os registros são separados por um único `<CR>` (código ASCII `0xD`), um único `<LF>` (código ASCII `0xA`) ou um `<CR><LF>` emparelhar.

O registro do cabeçalho deve conter os nomes exatos de cada campo de dados. Não são permitidos campos vazios na linha de cabeçalho. Os nomes de campos de dados não diferenciam maiúsculas de minúsculas. Todos os nomes de campos devem ser exclusivos.

Caracteres de espaço não podem ser usados como separadores de campo. Não são permitidos espaços no registro de cabeçalho. Nos registros de dados, todos os espaços no início ou no final de um campo de dados são considerados parte desse campo de dados.

Nos registros de dados, dois registros `<TAB>` caracteres indicam um campo vazio. Campos vazios podem herdar valores padrão dos atributos do catálogo ou dos padrões do servidor.

Os campos de dados podem, opcionalmente, ser colocados entre aspas duplas. Eles não devem conter `<CR>`, `<LF>`ou `<TAB>` caracteres, a menos que o valor de dados seja do tipo texto e esteja entre aspas duplas. Os campos de dados não devem ser codificados em HTTP.

Vários valores de dados no mesmo campo são separados por vírgulas, a menos que especificado de outra forma.

Colunas cujos nomes começam com &quot;.&quot; são ignorados. Isso permite armazenar dados em catálogos de imagem, o que não é de interesse para o Servidor de imagens. As colunas com nomes de cabeçalho desconhecidos são ignoradas e um aviso é gravado no arquivo de log.

Os nomes de campos podem consistir em qualquer combinação de letras ASCII, números, bem como &quot;-&quot; e &quot;_&quot;.

Uma ou mais colunas podem ser usadas como chaves de índice. Se a mesma chave ocorrer mais de uma vez no mesmo arquivo de dados, a instância mais recente prevalecerá.
