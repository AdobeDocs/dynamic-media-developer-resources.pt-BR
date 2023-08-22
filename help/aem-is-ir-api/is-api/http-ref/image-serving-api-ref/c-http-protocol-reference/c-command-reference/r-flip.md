---
title: girar
description: Inverter camada. Inverte a camada horizontalmente, verticalmente ou ambos, após aplicar cortar= e antes de girar= e estender=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---

# girar{#flip}

Inverter camada. Inverte a camada horizontalmente, verticalmente ou ambos, após aplicar cortar= e antes de girar= e estender=.

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>Inverter camada horizontalmente (esquerda-direita). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> Ud </span> </p> </td> 
  <td class="stentry"> <p>Inverter camada verticalmente (acima para baixo). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud </span> </p> </td> 
  <td class="stentry"> <p>Inverter horizontal e verticalmente. </p> </td> 
 </tr> 
</table>

Também pode ser aplicado a camadas de texto.

Alguns comandos, incluindo `extend=`, aplique implicitamente à camada 0 em vez da camada composta quando `layer=comp` está selecionada. Nesses cenários, todos os comandos atribuídos automaticamente à camada 0 são aplicados antes dos comandos que se aplicam a `layer=comp`. Assim, quando `layer=comp`, `extend=` é aplicado antes de `flip=`.

>[!NOTE]
>
>A camada invertida é posicionada com base na âncora da camada; valores flip= diferentes resultarão em posições de camada diferentes quando a âncora não estiver localizada no centro da camada.

## Propriedades {#section-294da2af7be746b5adfc35e29ee68217}

Camada. Se aplica à camada atual ou à imagem composta `layer=comp`. Ignorado pelas camadas de efeito.

## Padrão {#section-502044f81a89492198d5f12a738459ea}

Nenhum.

## Consulte também {#section-47f6484deccd420983df15ec163b4a83}

[girar=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
