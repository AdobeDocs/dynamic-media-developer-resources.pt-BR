---
title: Arquivos de dados do catálogo
description: Os arquivos de dados do catálogo podem ter qualquer nome e sufixo de arquivo (exceto .ini).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1fb91795-f699-40b4-a6bc-6eab3e1ecd1d
TQID: 'https://experienceleague.adobe.com/L4j9Svu1H5DOc55iImhT1g6hRQT6svB0V2kuRsU37GE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 301
ht-degree: 0%

---

# Arquivos de dados do catálogo{#catalog-data-files}

Os arquivos de dados do catálogo podem ter qualquer nome e sufixo de arquivo (exceto `.ini`).

Os arquivos de dados de catálogo podem ser mantidos prontamente usando aplicativos que suportam arquivos de dados de texto delimitados por tabulação, como o Microsoft® Excel e o Access.

Basicamente, um arquivo de dados de catálogo bidimensional consiste em um registro de cabeçalho que identifica as colunas de dados e qualquer número de registros de dados (linhas). Os campos no cabeçalho e nos registros de dados são separados por `<TAB>` caracteres. Os registros são separados por um único `<CR>` (código ASCII `0xD`), um único `<LF>` (código ASCII `0xA`) ou um par `<CR><LF>`.

O registro do cabeçalho deve conter os nomes exatos de cada campo de dados. Não são permitidos campos vazios na linha de cabeçalho. Os nomes de campos de dados não diferenciam maiúsculas de minúsculas. Todos os nomes de campos devem ser exclusivos.

Nenhum espaço em branco além dos separadores de campo `<TAB>` é permitido no cabeçalho e nos registros de dados.

Nos registros de dados, dois caracteres `<TAB>` adjacentes indicam um campo vazio. Campos vazios herdam valores padrão dos atributos do catálogo ou dos padrões do servidor.

Os campos de dados não devem conter `<CR>`, `<LF>` ou `<TAB>` caracteres, a menos que o valor de dados seja do tipo texto e esteja entre aspas simples ou duplas. Não codifique campos de dados em HTTP.

Vários valores de dados no mesmo campo são separados por vírgulas (&#39;,&#39;), a menos que especificado de outra forma.

As colunas cujos nomes começam com &#39;.&#39; são ignoradas; isso permite armazenar dados em catálogos de materiais que não são de interesse para a Renderização de imagem. As colunas com nomes de cabeçalho desconhecidos são ignoradas e um aviso é gravado no arquivo de log.

Os nomes de campos podem consistir em qualquer combinação de letras ASCII, números e &quot;-&quot; e &quot;_&quot;.

Uma ou mais colunas podem ser usadas como chaves de índice. Se a mesma chave ocorrer mais de uma vez no mesmo arquivo de dados, a instância mais recente prevalecerá.
