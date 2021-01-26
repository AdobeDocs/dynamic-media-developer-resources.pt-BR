---
description: Todos os arquivos de log são gravados na mesma pasta de log especificada com o diretório TC.
solution: Experience Manager
title: Registro do servidor
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# Registro do servidor{#server-logging}

Todos os arquivos de log são gravados na mesma pasta de log especificada com o diretório TC::.

Os arquivos de log normalmente são criados e girados diariamente. Os arquivos de log mais antigos na pasta de log são excluídos automaticamente após um número especificado de dias ( `TC::maxDays`).

ImportanteUma quantidade suficiente de espaço em disco deve ser reservada para arquivos de registro para evitar o esgotamento do espaço em disco. Pode ser necessário 1 a 2 GB/dia para um servidor altamente utilizado e configurações de log padrão.

O Servidor de plataforma e o Servidor de imagens criam os três tipos de arquivos de registro descritos abaixo.

Outros componentes do serviço de imagem e alguns outros pacotes do Dynamic Media, como os visualizadores do Dynamic Media, também podem criar arquivos de registro na mesma pasta. Esses arquivos de registro são para uso interno da Dynamic Media e podem ser solicitados pelo suporte técnico da Dynamic Media para fins de solução de problemas.

* [Log de acesso](c-access-log.md)
* [Registro de rastreamento](c-trace-log.md)
* [Log do servidor de imagens](c-image-server-log.md)

## Consulte também {#section-5ff5e46031b1461c92de24e632610d6d}

[Registro](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f) de acesso, Registro de  [depuração/rastreamento](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
