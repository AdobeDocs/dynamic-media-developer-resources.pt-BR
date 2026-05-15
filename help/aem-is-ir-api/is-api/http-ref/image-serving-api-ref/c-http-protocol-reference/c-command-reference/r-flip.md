---
title: girar
description: Inverter camada. Inverte a camada horizontalmente, verticalmente ou ambos, após aplicar cortar= e antes de girar= e estender=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
TQID: 'https://experienceleague.adobe.com/7RG0rzG40Mp5eQe663S5Ayyf99SIfSLPHgqbSL2Unn4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 0%

---

# girar{#flip}

Inverter camada. Inverte a camada horizontalmente, verticalmente ou ambos, após aplicar cortar= e antes de girar= e estender=.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>Inverter a camada horizontalmente (esquerda-direita). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">ud </span> </p> </td> 
  <td class="stentry"> <p>Inverter a camada verticalmente (para cima e para baixo). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud </span> </p> </td> 
  <td class="stentry"> <p>Inverter horizontal e verticalmente. </p> </td> 
 </tr> 
</table>

Ela também pode ser aplicada a camadas de texto.

Alguns comandos, incluindo `extend=`, aplicam-se implicitamente à camada 0 em vez da camada composta quando `layer=comp` é selecionado. Nesses cenários, todos os comandos atribuídos automaticamente à camada 0 são aplicados antes dos comandos que se aplicam a `layer=comp`. Assim, quando `layer=comp`, `extend=` é aplicado antes de `flip=`.

>[!NOTE]
>
>A camada invertida é posicionada com base na âncora da camada. Valores `flip=` diferentes resultam em posições de camada diferentes quando a âncora não está no centro da camada.

## Propriedades {#section-294da2af7be746b5adfc35e29ee68217}

Camada. Aplica-se à camada atual ou à imagem composta, se `layer=comp`. Ignorado pelas camadas de efeito.

## Padrão {#section-502044f81a89492198d5f12a738459ea}

Nenhum.

## Consulte também {#section-47f6484deccd420983df15ec163b4a83}

[girar=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [âncora=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
