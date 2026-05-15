---
title: Posicionamento da camada
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
TQID: https://experienceleague.adobe.com/SMf4V0AmxYIi0o0FZhMkRx9pprIxjJjEcCWT2agF1Bo
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 0f5947b3f28ba40cd479df463c843f7e99155d5e
workflow-type: tm+mt
source-wordcount: 91
ht-degree: 0%

---

# Posicionamento da camada{#layer-placement}

As camadas são posicionadas alinhando a origem da camada (origin=) com a origem da camada de plano de fundo em um deslocamento especificado por pos=.

Se a origem da camada não for especificada explicitamente para uma camada de imagem, ela será calculada da seguinte maneira:

1. Determine a âncora da imagem. Use `anchor=` ou, se não for especificado, `catalog::Anchor`.
1. Se a âncora de imagem estiver definida, aplique as transformações de camada e `extend=` para convertê-la em um valor origin=.
1. Se nenhuma âncora de imagem for definida, a origem da camada será colocada no centro do retângulo da camada (após a aplicação de `extend=`).

![Imagem de posicionamento da camada](assets/layerplacement.png)
