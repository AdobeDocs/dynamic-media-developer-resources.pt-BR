---
title: cabeçalho
description: Elemento de cabeçalho de resposta HTTP. Opcional em <rule> elementos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---

# cabeçalho{#header}

Elemento de cabeçalho de resposta HTTP. Opcional em `<rule>` elementos.

## Atributos {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*texto*&quot;** : Obrigatório. Especifica o nome do cabeçalho HTTP.

**`Action`= &quot;set&quot; |`"add"`**: Opcional. O padrão é `"set"`, que substitui qualquer valor de cabeçalho atual. Especificar `"add"` para que você possa anexar o valor do cabeçalho, separado por vírgula.

## Dados {#section-a387f541396c49d99c29692a38032914}

Valor do cabeçalho.

## Descrição {#section-fb2a8ad79bc5414d8bb0d0e8199f3269}

Permite adicionar novos cabeçalhos de resposta HTTP e adicionar ou substituir valores de cabeçalhos predefinidos. Os nomes e valores devem estar em conformidade com os padrões HTTP. Nenhuma codificação adicional é aplicada.

As variáveis de substituição do Servidor de imagens podem ser usadas no nome e no valor do cabeçalho. Isso permite controlar ambas as cadeias de caracteres da solicitação.

## Exemplo {#section-cb5b738b9b93407cb2f4d35af3e59c02}

A regra a seguir aplica um cabeçalho personalizado quando o valor do cabeçalho é especificado na solicitação como uma variável:

```
<rule OnMatch="continue">
   <expression>\$Edge-Control=</expression>
   <header Name="Edge-Control">$Edge-Control$</header>
</rule>
```

Essa regra é acionada pela seguinte solicitação, definindo o cabeçalho de resposta HTTP do `Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
