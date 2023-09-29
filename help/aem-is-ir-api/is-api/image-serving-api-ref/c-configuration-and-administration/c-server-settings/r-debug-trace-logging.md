---
title: Log de Debug_trace
description: Use estas configurações do servidor para depurar o log de rastreamento.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe1fc984-3c6b-4bd1-b5ba-630860ac7319
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Log de Debug_trace{#debug-trace-logging}

Use estas configurações do servidor para depurar o log de rastreamento.

>[!NOTE]
>
>O Adobe recomenda que você configure todos os arquivos de log para serem gravados na mesma pasta que `TC::directory`. Isso garante que todos os arquivos de registro do Servidor de imagens participem da rotação automática do arquivo de registro configurada com `TC::maxDays`, que impede a possível instabilidade do servidor devido a condições de espaço insuficiente em disco.

## SV::log - Caminho do Arquivo de Log de Rastreamento do Supervisor de Servidor {#section-3697bc480ff646e79cacc2812c55ef26}

Pasta e nome de arquivo base dos arquivos de log do Supervisor do Servidor. O caminho pode ser absoluto ou relativo a *[!DNL install_folder]*. O Supervisor de Servidor anexa um hífen e a data atual ( *[!DNL -yyyy-mm-dd]*) ao nome do arquivo (antes do sufixo do arquivo, se houver). O Adobe recomenda que você envie todos os arquivos de log para a mesma pasta que [!DNL Platform Server] arquivos de log ( `PS::LogFolder`) para usar o gerenciamento de arquivos de registro implementado pelo [!DNL Platform Server] (`PS::LogDays`). O padrão é [!DNL logs/Supervisor.log].

>[!NOTE]
>
>A nova pasta deve ser criada antes de alterar essa configuração. Verifique se as permissões de acesso estão definidas de modo que o Supervisor do Servidor tenha os privilégios de criação, leitura e gravação necessários.

## SV::tracelevel - Nível de Log de Rastreamento do Supervisor de Servidor {#section-36f8634741da4c618d67aa628b5fe474}

O nível de log pode ser 1, 2, 3 ou 4. O padrão é 2.

## IS::Log - Caminho do Arquivo de Log de Depuração do Servidor de Imagens {#section-73a3f09b77f2446c9f82207b7d8aec39}

Pasta e nome do arquivo base para arquivos de log de rastreamento do Servidor de imagens. O caminho pode ser absoluto ou relativo a *[!DNL install_folder]*. O ImageServer anexa um hífen e a data atual ( *[!DNL -yyyy-mm-dd]*) ao nome do arquivo (antes do sufixo do arquivo, se houver). A Adobe recomenda que você envie os arquivos de registro do Servidor de imagens para a mesma pasta que [!DNL Platform Server] arquivos de log ( `PS::LogFolder`) para usar o gerenciamento de arquivos de registro implementado pelo [!DNL Platform Server] (consulte `PS::LogDays`).

>[!NOTE]
>
>A nova pasta deve ser criada antes de alterar essa configuração. Verifique se as permissões de acesso estão definidas de modo que o Servidor de imagens tenha os privilégios de criação, leitura e gravação necessários.

## IS:TraceClient - Nível de Log de Depuração do Servidor de Imagens {#section-3851f1f68e404430985c629ac80534db}

O nível de log pode ser 1, 2, 3 ou 4 (o padrão é 2)

O nível 1 registra eventos relacionados à inicialização, desligamento e [!DNL Platform Server] conexões.

O nível 2 também registra a conexão com e a desconexão de imagens de origem.

O nível 3 adiciona o registro de solicitações para dados de pixel e entrega dos mesmos para o [!DNL Platform Server].

O nível 4 registra todas as mensagens recebidas do [!DNL Platform Server].

Os níveis 3 e 4 devem ser usados somente para fins de depuração, pois os arquivos de registro podem se tornar grandes.

## IS::TraceStatsInterval - Intervalo de Log de Estatísticas do Servidor de Imagens {#section-1d8df96d61044e33a5b2b2b0309c2d59}

O Servidor de Imagens grava estatísticas de memória em seu arquivo de log de rastreamento no intervalo especificado por essa configuração. O intervalo válido é de 5 a 86.400 segundos.
