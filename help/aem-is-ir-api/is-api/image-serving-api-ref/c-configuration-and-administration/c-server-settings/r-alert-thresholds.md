---
description: Use essas configurações do servidor para definir limites de alerta.
seo-description: Use essas configurações do servidor para definir limites de alerta.
seo-title: Limites de alerta
solution: Experience Manager
title: Limites de alerta
uuid: 032cb396-1a03-4ba9-82d6-ed2cb06e8cf2
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---


# Limites de alerta{#alert-thresholds}

Use essas configurações do servidor para definir limites de alerta.

## AS: monitorAlertGenerator.maxAverageResponseTime -Tempo de Resposta LimiteAS: monitorAlertGenerator.maxAverageResponseTime -Tempo de Resposta {#section-35111039ac6c4a63ba23fc2c828ab726}

Um alerta de tempo de resposta é emitido quando o tempo médio para processar uma solicitação durante o intervalo de amostragem excede o limite definido aqui. Expresso em ms; número inteiro 0 ou maior. Valores típicos estão entre 100 e 1000 ms, dependendo da complexidade das operações.

>[!NOTE]
>
>Solicitações que resultam em status de resposta 4xx ou 5xx não são consideradas para esse alerta.

## AS::monitorAlertGenerator.maxErrorRate - Error Response Rate ThresholdAS::monitorAlertGenerator.maxErrorRate - Error Response Rate {#section-76ba77fd3102419395e0f86719a1f3ec}

Um alerta de erro é emitido quando a proporção de respostas de erro HTTP para o total de respostas durante o intervalo de amostragem excede o limite especificado.

Valor real entre 0.0 e 1.0. Normalmente, é definido como entre 0.005 e 0.1. Defina como 1 para desativar alertas de erro.

## AS::monitorAlertGenerator.minRequestRate - Limite de tráfego baixo {#section-8dfb89ed138640fd86f5ce1dae2a533e}

Um alerta de tráfego mínimo é enviado quando o número médio de solicitações por segundo recebidas durante o intervalo de amostragem atual cair abaixo desse limite. Desative o alerta definindo esse valor como 0. Expresso em solicitações por segundo. Valor real 0 ou maior.

## AS::monitorAlertGenerator.minFreeHeapSpace -Limite de espaço livre do heap {#section-ce6705045f6842769030ccb1894594cc}

Especifica o espaço mínimo gratuito de heap Java. Um alerta de prioridade é enviado imediatamente após um ciclo de coleta de lixo Java quando o espaço livre de heap estiver abaixo desse limite. Recomenda-se 50 MB para a operação segura do Servidor da Plataforma. Manter o espaço livre de heap acima desse valor reduz a frequência dos ciclos de coleta de lixo, o que pode melhorar o desempenho geral do servidor. Valor inteiro em bytes, 0 ou maior.

## AS::monitorAlertGenerator.maxOverlap - Número máximo de solicitações simultâneas {#section-ddc6925bff944758ab19bcc9cf3f2589}

Um alerta de sobreposição é acionado quando o número médio de solicitações processadas simultaneamente durante o intervalo de média excede esse limite. Uma alta sobreposição pode indicar uma possível condição de sobrecarga do servidor.

Valor inteiro 1 ou maior. O intervalo típico é de 20 a 50, dependendo da taxa de ocorrência do cache e da complexidade da solicitação.

## AS::monitorAlertGenerator.lockedThreshold - Limite de Solicitação Bloqueada {#section-012a1c9937d445708380339279c62d80}

Especifica o número de segundos que uma solicitação deve estar pendente antes de ser considerada bloqueada ou suspensa. Um alerta de solicitação bloqueada é emitido se, no final de um intervalo de média, pelo menos uma solicitação estiver pendente por mais do que o período especificado. Valor inteiro positivo em ms.

Para contabilizar solicitações de renderização complexas e solicitações que envolvam a obtenção de dados de servidores HTTP estrangeiros, é recomendável definir esse valor como pelo menos 30 segundos (a menos que essa condição seja detectada por esse alerta).
