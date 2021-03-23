---
description: Todos os arquivos de log são gravados na mesma pasta de log especificada com o diretório TC.
solution: Experience Manager
title: Registro do servidor
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---


# Registro do servidor{#server-logging}

Todos os arquivos de log são gravados na mesma pasta de log especificada com o diretório TC::.

Os arquivos de log normalmente são criados e rodados diariamente. Arquivos de log mais antigos na pasta de log são excluídos automaticamente após um número especificado de dias ( `TC::maxDays`).

Importante Uma quantidade suficiente de espaço em disco deve ser reservada para arquivos de log para evitar a falta de espaço em disco. Pode ser necessário de 1 a 2 GB/dia para um servidor de uso intenso e configurações de log padrão.

O Servidor de plataforma e o Servidor de imagem criam os três tipos de arquivos de log descritos abaixo.

Outros componentes do Image Serving e alguns outros pacotes do Dynamic Media, como os Visualizadores do Dynamic Media, também podem criar arquivos de log na mesma pasta. Esses arquivos de log são para uso interno da Dynamic Media e podem ser solicitados pelo suporte técnico da Dynamic Media para fins de solução de problemas.

* [Log de acesso](c-access-log.md)
* [Log de rastreamento](c-trace-log.md)
* [Log do servidor de imagens](c-image-server-log.md)

## Consulte também {#section-5ff5e46031b1461c92de24e632610d6d}

[Registro de acesso](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f), Registro de  [depuração/rastreamento](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
