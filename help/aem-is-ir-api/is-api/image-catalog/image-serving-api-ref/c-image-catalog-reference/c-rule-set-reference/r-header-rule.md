---
description: Elemento do cabeçalho de resposta HTTP. Opcional em elementos <rule> .
solution: Experience Manager
title: header
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# header{#header}

Elemento do cabeçalho de resposta HTTP. Opcional em elementos `<rule>`.

## Atributos {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*text*&quot;** : Obrigatório. Especifica o nome do cabeçalho HTTP.

**`Action`= &quot;set&quot; |`"add"`**: Opcional. O padrão é `"set"`, que substitui qualquer valor de cabeçalho atual. Especifique `"add"` para anexar o valor do cabeçalho, separado por vírgula.

## Dados {#section-a387f541396c49d99c29692a38032914}

Valor do cabeçalho.

## Descrição {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

Permite adicionar novos cabeçalhos de resposta HTTP, bem como adicionar ou substituir valores de cabeçalhos predefinidos. Nomes e valores devem estar em conformidade com os padrões HTTP. Nenhuma codificação adicional será aplicada.

As variáveis de substituição do Image Serving podem ser usadas no nome do cabeçalho e no valor do cabeçalho. Isso permite controlar ambas as cadeias de caracteres da solicitação.

## Exemplo {#section-cb5b738b9b93407cb2f4d35af3e59c02}

A regra a seguir aplica um cabeçalho personalizado quando o valor do cabeçalho é especificado na solicitação como uma variável:

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

Essa regra é acionada pela seguinte solicitação, definindo o cabeçalho de resposta HTTP `Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
