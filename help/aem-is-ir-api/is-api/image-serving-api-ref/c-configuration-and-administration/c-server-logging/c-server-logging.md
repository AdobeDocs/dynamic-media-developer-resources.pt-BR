---
description: Todos os arquivos de log são gravados na mesma pasta de log especificada com o diretório TC.
seo-description: Todos os arquivos de log são gravados na mesma pasta de log especificada com o diretório TC.
seo-title: Registro do servidor
solution: Experience Manager
title: Registro do servidor
topic: Scene7 Image Serving - Image Rendering API
uuid: f6145737-e4c3-4533-9be5-5b5a0202fe33
translation-type: tm+mt
source-git-commit: 5717550d2dea8ec086875e770ff8f200aaa75ff3
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---


# Registro do servidor{#server-logging}

Todos os arquivos de log são gravados na mesma pasta de log especificada com o diretório TC::.

Os arquivos de log normalmente são criados e girados diariamente. Os arquivos de log mais antigos na pasta de log são excluídos automaticamente após um número especificado de dias ( `TC::maxDays`).

ImportanteUma quantidade suficiente de espaço em disco deve ser reservada para arquivos de registro para evitar o esgotamento do espaço em disco. Pode ser necessário 1 a 2 GB/dia para um servidor altamente utilizado e configurações de log padrão.

O Servidor de plataforma e o Servidor de imagens criam os três tipos de arquivos de registro descritos abaixo.

Outros componentes do serviço de imagem e alguns outros pacotes do Scene7, como os visualizadores do Scene7, também podem criar arquivos de registro na mesma pasta. Esses arquivos de registro são para uso interno da Scene7 e podem ser solicitados pelo Suporte da Scene7 para fins de solução de problemas.

* [Log de acesso](c-access-log.md)
* [Registro de rastreamento](c-trace-log.md)
* [Log do servidor de imagens](c-image-server-log.md)

## Consulte também {#section-5ff5e46031b1461c92de24e632610d6d}

[Registro](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f) de acesso, Registro de  [depuração/rastreamento](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
