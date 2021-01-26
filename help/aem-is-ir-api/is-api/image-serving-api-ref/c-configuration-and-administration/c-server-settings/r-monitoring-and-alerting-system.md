---
description: Use essas configurações do servidor para configurar o sistema de monitoramento e alerta.
seo-description: Use essas configurações do servidor para configurar o sistema de monitoramento e alerta.
seo-title: Sistema de acompanhamento e alerta
solution: Experience Manager
title: Sistema de acompanhamento e alerta
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 944c7d53-09ec-443e-ac8c-85684d8fda0f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---


# Sistema de monitoramento e alerta{#monitoring-and-alerting-system}

Use essas configurações do servidor para configurar o sistema de monitoramento e alerta.

## AS::monitorAlertGenerator.enableGlobalAlerting - Ativação do Sistema de Alertas {#section-612f8ea61794426ab205e22e5f665fa9}

Ative a notificação por email definindo como &quot;true&quot; e definindo as configurações de notificação por email. A configuração para `false` desativa todos os alertas de e-mail - isso pode ser útil quando um servidor é removido para manutenção. Booleano.

## AS::mailSender.host - Host SMTP {#section-151df07e7b44446581339bb7abeeba7a}

O endereço IP do servidor de email SMTP.

## AS::mailSender.port- Porta SMTP {#section-4b25efca8fd84d5c92dafacd0555e99d}

A porta de escuta do servidor de email SMTP.

## AS::monitorAlertGenerator.messageTo - Recipient de mensagem {#section-0017bbaa15434117a70900c3f1163960}

Um ou mais endereços de email para os quais os alertas devem ser enviados. Use ponto-e-vírgula como separadores.

## AS::monitorAlertGenerator.messageFrom - Remetente de mensagem {#section-db320cba4ac2438ca1cfe6abce4aed87}

O endereço de email que deve ser usado no campo de email **[!UICONTROL From]**.

## AS::monitorAlertGenerator.alertInterval - Intervalo de monitoramento {#section-99cb2e3380c1499e9d5aec3671ed73c7}

O sistema de monitoramento acumulará as condições de alerta durante o intervalo de alerta e enviará um email de alerta contendo todos os alertas acumulados ao final de cada intervalo. Milissegundos, valor inteiro, 60000 ou maior. Normalmente definido como 5 ou 10 minutos.

## AS::monitorAlertGenerator.heapSpaceResetInterval - Intervalo de Alerta do Espaço de Heap {#section-fd5a2bf04ed44fdcaef20f77084151a8}

Tempo mínimo após um alerta de espaço heap antes que outro seja emitido. Tempo de intervalo em ms. Valor inteiro, 0 ou maior.

## AS::monitorAlertGenerator.minTrafficForAlerts - tráfego mínimo para ativar o alerta {#section-8b4db2d6f96642309ca35c49eb3ab230}

Solicitações por segundo. Nenhum tempo de resposta e alertas de erro serão emitidos se o tráfego cair abaixo desse limite. Defina como 0 para enviar alertas de tempo de resposta e de erro independentemente do volume de tráfego. Valor real 0 ou maior.
