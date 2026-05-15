---
title: Recurso de impressão
description: O visualizador permite exibir o conteúdo do catálogo em uma impressora.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d7c8a0da-ad8b-440e-b27b-ea85dd975d9d
TQID: 'https://experienceleague.adobe.com/5eIB7D6O7-d8prjO0MJ9PzUU9TPQe7SZcZAEtznPsv4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 0%

---

# Recurso de impressão{#print-feature}

O visualizador permite exibir o conteúdo do catálogo em uma impressora.

O recurso de impressão é acionado por um botão dedicado na barra de ferramentas. Clicar no botão permite que o usuário escolha um intervalo de impressão e o número de páginas por folha.

A qualidade da impressão pode ser ajustada usando o parâmetro de configuração `printquality`. Não é recomendável configurar `printquality` para valores maiores que o padrão. Isso ocorre porque ele leva a um alto consumo de memória pelo navegador da Web no sistema do cliente. Além disso, verifique se o tamanho máximo de resposta da imagem definido para sua empresa Dynamic Media Classic é maior que o valor configurado `printquality`.

>[!NOTE]
>
>O recurso de impressão só está disponível em sistemas desktop, exceto no Internet Explorer 9.
