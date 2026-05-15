---
title: cabeçalho
description: Elemento de cabeçalho de resposta HTTP. Opcional em elementos <rule>.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 40849602-16b2-471b-9128-14653e84a45a
TQID: 'https://experienceleague.adobe.com/-hGRn7zVjm8eavZIwBoiAuCqoSNYIFSSlQaSP6wuHXs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 137
ht-degree: 0%

---

# cabeçalho{#header}

Elemento de cabeçalho de resposta HTTP. Opcional em `<rule>` elementos.

## Atributos {#section-6e903ab4c64f4b1488b8ae74274f50a6}

**`Name`= &quot;*texto*&quot;** : Obrigatório. Especifica o nome do cabeçalho HTTP.

**`Action`= &quot;definido&quot; |`"add"`**: Opcional. O padrão é `"set"`, que substitui qualquer valor de cabeçalho atual. Especifique `"add"` para que você possa anexar o valor do cabeçalho, separado por vírgula.

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

Esta regra é disparada pela seguinte solicitação, definindo o cabeçalho de resposta HTTP `Edge-Control::no-store`:

`http://server/is/image/cat/id?$Edge-Control=no-store`
