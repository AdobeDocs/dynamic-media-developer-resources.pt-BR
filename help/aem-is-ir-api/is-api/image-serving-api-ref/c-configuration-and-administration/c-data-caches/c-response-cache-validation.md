---
description: As entradas de cache são atualizadas automaticamente usando a validação de cache com base em catálogo ou em expiração, conforme selecionado com o atributo CacheValidationPolicy (em default.ini ou no arquivo .ini de um catálogo de imagens específico).
solution: Experience Manager
title: Validação do cache de resposta
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d2baa6e6-2700-450f-af1e-88b6d33d0e0c
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---

# Validação do cache de resposta{#response-cache-validation}

As entradas de cache são atualizadas automaticamente usando a validação de cache baseada em catálogo ou em expiração, conforme selecionado com o atributo::CacheValidationPolicy (em default.ini ou no arquivo .ini de um catálogo de imagens específico).

Com a validação baseada em catálogo, uma entrada de cache existente é considerada obsoleta se `catalog::LastModified` (ou `attribute::LastModified`ou a hora de modificação do arquivo do [!DNL catalog.ini] ) é mais recente do que a hora em que a entrada de cache foi criada.

Com a validação baseada em expiração, uma entrada de cache fica obsoleta após 5 minutos desde a validação mais recente. Em ambos os casos, o servidor valida entradas de cache obsoletas verificando as datas de todos os arquivos de imagem envolvidos na criação da solicitação. Se as datas do arquivo não tiverem sido alteradas, o carimbo de data e hora da entrada do cache será atualizado e a data do cache será considerada válida.

Para aplicativos típicos que envolvem principalmente imagens registradas em catálogos de imagens, a validação baseada em catálogo oferece uma vantagem de desempenho. Os aplicativos que não envolvem catálogos de imagens devem usar a validação de cache com base em expiração. Uma maneira de conseguir isso é definir `attribute::cacheValidationPolicy=0` in [!DNL default.ini], e para `1` em todos os arquivos específicos do catálogo de imagens.

As entradas de cache se tornam inválidas e estão sujeitas a nova geração quando uma entrada de catálogo envolvida na solicitação é alterada de uma forma que provavelmente causaria uma alteração na imagem de resposta. Por exemplo, o conteúdo de `catalog::Modifier` alterações.

>[!NOTE]
>
>As imagens Dynamic Media pyramid TIFF (PTIFF) mantêm a data do arquivo internamente no cabeçalho do arquivo para fins de validação. O tempo de modificação do arquivo mantido pelo sistema de arquivos é usado para verificar se um arquivo não PTIFF foi alterado.

Somente arquivos de imagem participam do processo de validação de cache. As alterações nos arquivos de fonte ou nos arquivos de perfil ICC não causam a invalidação automática das entradas de cache.
