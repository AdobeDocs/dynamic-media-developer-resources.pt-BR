---
description: As entradas de cache são atualizadas automaticamente usando a validação de cache com base em catálogo ou em expiração, conforme selecionado com o atributo CacheValidationPolicy (em default.ini ou no arquivo .ini de um catálogo de imagens específico).
solution: Experience Manager
title: Validação do cache de resposta
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d2baa6e6-2700-450f-af1e-88b6d33d0e0c
TQID: 'https://experienceleague.adobe.com/VnvYNkc3yijayG8tnJKHsp94Qto8VZj9OkIgfIv1Kc0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 311
ht-degree: 0%

---

# Validação do cache de resposta{#response-cache-validation}

As entradas de cache são atualizadas automaticamente usando a validação de cache baseada em catálogo ou em expiração, conforme selecionado com o atributo::CacheValidationPolicy (em default.ini ou no arquivo .ini de um catálogo de imagens específico).

Com a validação baseada em catálogo, uma entrada de cache existente será considerada obsoleta se `catalog::LastModified` (ou `attribute::LastModified`, ou a hora de modificação de arquivo do arquivo [!DNL catalog.ini]) for mais recente do que a hora em que a entrada de cache foi criada.

Com a validação baseada em expiração, uma entrada de cache fica obsoleta após 5 minutos desde a validação mais recente. Em ambos os casos, o servidor valida entradas de cache obsoletas verificando as datas de todos os arquivos de imagem envolvidos na criação da solicitação. Se as datas do arquivo não tiverem sido alteradas, o carimbo de data e hora da entrada do cache será atualizado e a data do cache será considerada válida.

Para aplicativos típicos que envolvem principalmente imagens registradas em catálogos de imagens, a validação baseada em catálogo oferece uma vantagem de desempenho. Os aplicativos que não envolvem catálogos de imagens devem usar a validação de cache com base em expiração. Uma maneira de conseguir isso é definir `attribute::cacheValidationPolicy=0` em [!DNL default.ini] e `1` em todos os arquivos de catálogo de imagens específicos.

As entradas de cache se tornam inválidas e estão sujeitas a nova geração quando uma entrada de catálogo envolvida na solicitação é alterada de uma forma que provavelmente causaria uma alteração na imagem de resposta. Por exemplo, o conteúdo de `catalog::Modifier` é alterado.

>[!NOTE]
>
>As imagens da TIFF de pirâmide do Dynamic Media (PTIFF) mantêm a data do arquivo internamente no cabeçalho do arquivo para fins de validação. O tempo de modificação do arquivo mantido pelo sistema de arquivos é usado para verificar se um arquivo não PTIFF foi alterado.

Somente arquivos de imagem participam do processo de validação de cache. As alterações nos arquivos de fonte ou nos arquivos de perfil ICC não causam a invalidação automática das entradas de cache.
