---
description: Todos os arquivos de log são gravados na mesma pasta de log especificada com o diretório TC.
solution: Experience Manager
title: Registro do servidor
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 5be30dd6-e540-4189-9379-7465ac7198ce
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# Registro do servidor{#server-logging}

Todos os arquivos de log são gravados na mesma pasta de log especificada com TC::diretory.

Os arquivos de registro normalmente são criados e rotacionados diariamente. Os arquivos de log mais antigos na pasta de log são excluídos automaticamente após um número especificado de dias ( `TC::maxDays`).

Importante: uma quantidade suficiente de espaço em disco deve ser reservada para os arquivos de log para evitar ficar sem espaço em disco. Pode ser necessário de 1 a 2 GB/dia para um servidor muito usado e configurações de log padrão.

O [!DNL Platform Server] e o Servidor de imagens criam os três tipos de arquivos de log descritos abaixo.

Outros componentes do Servidor de imagens e determinados outros pacotes do Dynamic Media, como os Visualizadores do Dynamic Media, também podem criar arquivos de log na mesma pasta. Esses arquivos de registro são para uso interno do Dynamic Media e podem ser solicitados pelo suporte técnico do Dynamic Media para fins de solução de problemas.

* [Log de acesso](c-access-log.md)
* [Log de rastreamento](c-trace-log.md)
* [Log do servidor de imagens](c-image-server-log.md)

## Consulte também {#section-5ff5e46031b1461c92de24e632610d6d}

[Log de Acesso](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f), [Log de Depuração/Rastreamento](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
