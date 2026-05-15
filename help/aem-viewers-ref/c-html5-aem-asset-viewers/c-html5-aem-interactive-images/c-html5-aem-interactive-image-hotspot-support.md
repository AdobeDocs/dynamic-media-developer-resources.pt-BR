---
title: Suporte a pontos de acesso
description: Suporte a pontos de acesso
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
TQID: 'https://experienceleague.adobe.com/kvYBwi70uYXIK8D6MeNgZN74h3X6jBfmOLj1SjlKEzs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 0%

---

# Suporte a pontos de acesso{#hotspot-support}

O visualizador suporta a renderização de ícones de pontos de acesso na parte superior da exibição principal. A aparência dos ícones de ponto de acesso é controlada por meio do CSS, conforme descrito na seção Pontos de acesso.

Consulte [Pontos de acesso](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

Os pontos de acesso podem ativar um recurso de Visualização rápida na página da Web de hospedagem acionando um retorno de chamada do JavaScript ou redirecionar um usuário para uma página da Web externa.

## Pontos de acesso do Quickview {#section-cda48fc9730142d0bb3326bac7df3271}

Esses tipos de hotspots devem ser criados usando o tipo de ação &quot;Quickview&quot; na Mídia dinâmica, do Adobe Experience Manager Assets - Sob demanda. Quando um usuário ativa esse ponto de acesso, o visualizador executa o retorno de chamada do JavaScript `quickViewActivate` e passa os dados do ponto de acesso para ele. Espera-se que a página da Web de incorporação acompanhe esse retorno de chamada. Ao acionar a página, ele abre sua própria implementação do Quickview.

## Redirecionar para página da Web externa {#section-ef820c71251e4215800bb99c0c9ebe16}

Pontos de acesso criados para o tipo de ação &quot;Visualização rápida&quot; no Dynamic Media do Experience Manager Assets - On-demand redireciona o usuário para um URL externo. Dependendo das configurações feitas durante a criação, o URL é aberto em uma nova guia do navegador, na mesma janela ou na janela do navegador nomeada.
