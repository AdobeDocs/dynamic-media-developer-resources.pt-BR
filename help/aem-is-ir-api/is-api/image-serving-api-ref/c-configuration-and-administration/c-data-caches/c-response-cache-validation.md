---
description: As entradas de cache são atualizadas automaticamente usando a validação de cache baseada em catálogo ou em expiração, conforme selecionado com o atributo CacheValidationPolicy (em default.ini ou o arquivo .ini de um catálogo de imagem específico).
seo-description: As entradas de cache são atualizadas automaticamente usando a validação de cache baseada em catálogo ou em expiração, conforme selecionado com o atributo CacheValidationPolicy (em default.ini ou o arquivo .ini de um catálogo de imagem específico).
seo-title: Validação do cache de resposta
solution: Experience Manager
title: Validação do cache de resposta
uuid: d1aad5ae-f0fa-489b-a48b-b0ac8c8f43bb
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---


# Validação do cache de resposta{#response-cache-validation}

As entradas de cache são atualizadas automaticamente usando a validação de cache baseada em catálogo ou em expiração, conforme selecionado com o atributo::CacheValidationPolicy (em default.ini ou o arquivo .ini de um catálogo de imagem específico).

Com a validação baseada em catálogo, uma entrada de cache existente é considerada obsoleta se `catalog::LastModified` (ou `attribute::LastModified`, ou o tempo de modificação de arquivo do arquivo [!DNL catalog.ini]) for mais recente do que o momento em que a entrada de cache foi criada.

Com a validação baseada em expiração, uma entrada de cache torna-se obsoleta após 5 minutos desde a validação mais recente. Em ambos os casos, o servidor valida entradas obsoletas de cache verificando as datas do arquivo de todos os arquivos de imagem envolvidos na criação da solicitação. Se as datas do arquivo não tiverem sido alteradas, o carimbo de data e hora da entrada do cache será atualizado e a data em cache será considerada válida.

Para aplicativos típicos que envolvem a maioria das imagens registradas em catálogos de imagens, a validação baseada em catálogo fornece uma vantagem de desempenho. Os aplicativos que não envolvem catálogos de imagens devem usar a validação de cache com base em expiração. Uma maneira de fazer isso é definir `attribute::cacheValidationPolicy=0` em [!DNL default.ini] e para `1` em todos os arquivos de catálogo de imagem específicos.

As entradas de cache se tornam inválidas e estão sujeitas a regeração quando uma entrada de catálogo envolvida na solicitação muda de uma maneira que provavelmente causaria uma alteração da imagem de resposta. Por exemplo, o conteúdo de `catalog::Modifier` é alterado.

>[!NOTE]
>
>As imagens TIFF (PTIFF) da pirâmide Dynamic Media mantêm a data do arquivo internamente no cabeçalho do arquivo para fins de validação. O tempo de modificação de arquivos mantido pelo sistema de arquivos é usado para verificar se um arquivo não PTIFF foi alterado.

Somente arquivos de imagem participam do processo de validação do cache. As alterações nos arquivos de fonte ou nos arquivos de perfil ICC não causam a invalidação automática de entradas de cache.
