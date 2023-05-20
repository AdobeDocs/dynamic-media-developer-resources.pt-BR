---
description: Use essas configurações do servidor para definir limites de alerta.
solution: Experience Manager
title: Limites de alerta
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1ae76692-2688-4902-82a0-d0751408eee7
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# Limites de alerta{#alert-thresholds}

Use essas configurações do servidor para definir limites de alerta.

## AS: monitorAlertGenerator.maxAverageResponseTime -Response Time ThresholdAS:: monitorAlertGenerator.maxAverageResponseTime -Response Time {#section-35111039ac6c4a63ba23fc2c828ab726}

Um alerta de tempo de resposta é emitido quando o tempo médio para processar uma solicitação durante o intervalo de amostragem excede o limite definido aqui. Expressa em ms; número inteiro 0 ou maior. Os valores típicos estão entre 100 e 1000 ms, dependendo da complexidade das operações.

>[!NOTE]
>
>Solicitações que resultam em status de resposta 4xx ou 5xx não são consideradas para este alerta.

## AS::monitorAlertGenerator.maxErrorRate - Limite de Taxa de Resposta de ErroAS::monitorAlertGenerator.maxErrorRate - Taxa de Resposta de Erro {#section-76ba77fd3102419395e0f86719a1f3ec}

Um alerta de erro é emitido quando a proporção de respostas de erro HTTP para o total de respostas durante o intervalo de amostragem excede o limite especificado.

Valor real entre 0,0 e 1,0. Normalmente definido como entre 0,005 e 0,1. Defina como 1 para desativar alertas de erro.

## AS::monitorAlertGenerator.minRequestRate - Limite de Tráfego Baixo {#section-8dfb89ed138640fd86f5ce1dae2a533e}

Um alerta de tráfego mínimo é enviado quando o número médio de solicitações por segundo recebidas durante o intervalo de amostragem atual cai abaixo desse limite. Desative o alerta definindo este valor como 0. Expressa em solicitações por segundo. Valor real 0 ou maior.

## AS::monitorAlertGenerator.minFreeHeapSpace - Limite de espaço livre no Heap {#section-ce6705045f6842769030ccb1894594cc}

Especifica o espaço livre mínimo de heap do Java. Um alerta de prioridade é enviado imediatamente após um ciclo de coleta de lixo Java quando o espaço livre em heap está abaixo desse limite. 50 MB são recomendados para a operação segura do [!DNL Platform Server]. Manter o espaço de heap livre acima desse valor reduz a frequência dos ciclos de coleta de lixo, o que pode melhorar o desempenho geral do servidor. Valor inteiro em bytes, 0 ou maior.

## AS::monitorAlertGenerator.maxOverlap - Número Máximo de Solicitações Simultâneas {#section-ddc6925bff944758ab19bcc9cf3f2589}

Um alerta de sobreposição é disparado quando o número médio de solicitações processadas simultaneamente durante o intervalo de média excede esse limite. Uma sobreposição alta pode indicar uma possível condição de sobrecarga do servidor.

Valor inteiro 1 ou maior. O intervalo típico é de 20 a 50, dependendo da taxa de ocorrência do cache e da complexidade da solicitação.

## AS::monitorAlertGenerator.lockedThreshold - Limite de Solicitações Bloqueadas {#section-012a1c9937d445708380339279c62d80}

Especifica o número de segundos que uma solicitação deve permanecer pendente antes de ser considerada bloqueada ou suspensa. Um alerta de solicitação bloqueada é emitido se, no final de um intervalo de média, pelo menos uma solicitação estiver pendente por mais tempo do que o período especificado. Valor inteiro positivo em ms.

Para levar em conta solicitações de renderização complexas e solicitações que envolvem a obtenção de dados de servidores HTTP externos, é recomendável definir esse valor para pelo menos 30 segundos (a menos que essa condição seja detectada por esse alerta).
