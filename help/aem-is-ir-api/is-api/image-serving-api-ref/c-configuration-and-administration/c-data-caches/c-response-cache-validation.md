---
description: As entradas de cache são atualizadas automaticamente usando a validação de cache baseada em catálogo ou em expiração, conforme selecionado com o atributo CacheValidationPolicy (em default.ini ou o arquivo .ini de um catálogo de imagem específico).
seo-description: As entradas de cache são atualizadas automaticamente usando a validação de cache baseada em catálogo ou em expiração, conforme selecionado com o atributo CacheValidationPolicy (em default.ini ou o arquivo .ini de um catálogo de imagem específico).
seo-title: Validação do cache de respostas
solution: Experience Manager
title: Validação do cache de respostas
topic: Scene7 Image Serving - Image Rendering API
uuid: d1aad5ae-f0fa-489b-a48b-b0ac8c8f43bb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Validação do cache de respostas{#response-cache-validation}

As entradas de cache são atualizadas automaticamente usando a validação de cache baseada em catálogo ou em expiração, conforme selecionado com o atributo::CacheValidationPolicy (em default.ini ou o arquivo .ini de um catálogo de imagem específico).

Com a validação baseada em catálogo, uma entrada de cache existente é considerada obsoleta se `catalog::LastModified` (ou `attribute::LastModified`, ou a hora de modificação do arquivo do [!DNL catalog.ini] arquivo) for mais recente do que a hora em que a entrada de cache foi criada.

Com a validação baseada em expiração, uma entrada de cache fica obsoleta após 5 minutos desde a validação mais recente. Em ambos os casos, o servidor valida as entradas obsoletas do cache verificando as datas do arquivo de todos os arquivos de imagem envolvidos na criação da solicitação. Se as datas do arquivo não tiverem sido alteradas, o carimbo de data e hora da entrada do cache será atualizado e a data em cache será considerada válida.

Para aplicativos típicos que envolvem principalmente imagens registradas em catálogos de imagens, a validação baseada em catálogo oferece uma vantagem de desempenho. Aplicativos que não envolvem catálogos de imagens devem usar a validação de cache com base em expiração. Uma maneira de conseguir isso é definir `attribute::cacheValidationPolicy=0` em [!DNL default.ini]e `1` em todos os arquivos de catálogo de imagens específicos.

As entradas de cache se tornam inválidas e estão sujeitas a nova geração quando uma entrada de catálogo envolvida na solicitação muda de uma forma que provavelmente causaria uma alteração na imagem de resposta. Por exemplo, o conteúdo das `catalog::Modifier` alterações.

>[!NOTE] {class=&quot;- tópico/observação &quot;}
>
>As imagens TIFF (PTIFF) da pirâmide Scene7 mantêm a data do arquivo internamente no cabeçalho do arquivo para fins de validação. O tempo de modificação do arquivo mantido pelo sistema de arquivos é usado para verificar se um arquivo não PTIFF foi alterado.

Somente arquivos de imagem participam do processo de validação do cache. As alterações nos arquivos de fonte ou nos arquivos de perfil ICC não causam a invalidação automática das entradas de cache.
