---
description: Use essas configurações do servidor para depurar o log de rastreamento.
solution: Experience Manager
title: Registro do Debug_trace
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: fe1fc984-3c6b-4bd1-b5ba-630860ac7319
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Registro do Debug_trace{#debug-trace-logging}

Use essas configurações do servidor para depurar o log de rastreamento.

>[!NOTE]
>
>É recomendável configurar todos os arquivos de log a serem gravados na mesma pasta que `TC::directory`. Isso garante que todos os arquivos de log do Image Serving participem da rotação automática do arquivo de log configurada com `TC::maxDays`, o que evitará a possível instabilidade do servidor devido a condições de falta de espaço em disco.

## SV::log - Caminho do Arquivo de Log de Rastreamento do Supervisor do Servidor {#section-3697bc480ff646e79cacc2812c55ef26}

Nome da pasta e do arquivo base para arquivos de log do Server Supervisor. O caminho pode ser absoluto ou relativo a *[!DNL install_folder]*. O Supervisor de Servidor anexará um hífen e a data atual ( *[!DNL -yyyy-mm-dd]*) ao nome do arquivo (antes do sufixo do arquivo, se houver). É recomendável enviar todos os arquivos de log para a mesma pasta como [!DNL Platform Server] arquivos de log ( `PS::LogFolder`) para aproveitar o gerenciamento de arquivos de log implementado pela [!DNL Platform Server] ( `PS::LogDays`). O padrão é [!DNL logs/Supervisor.log].

>[!NOTE]
>
>A nova pasta deve ser criada antes de alterar essa configuração. Verifique se as permissões de acesso estão definidas para que o Supervisor de Servidor tenha os privilégios de criação, leitura e gravação necessários.

## SV::tracelevel - Nível de Log de Rastreamento de Supervisor de Servidor {#section-36f8634741da4c618d67aa628b5fe474}

O nível de log pode ser 1, 2, 3 ou 4. O padrão é 2.

## IS::Log - Caminho do Arquivo de Log de Depuração do Servidor de Imagens {#section-73a3f09b77f2446c9f82207b7d8aec39}

Nome da pasta e do arquivo base para os arquivos de log de rastreamento do Servidor de imagens. O caminho pode ser absoluto ou relativo a *[!DNL install_folder]*. O ImageServer anexará um hífen e a data atual ( *[!DNL -yyyy-mm-dd]*) ao nome do arquivo (antes do sufixo do arquivo, se houver). É recomendável enviar arquivos de log do Servidor de Imagens para a mesma pasta como [!DNL Platform Server] arquivos de log ( `PS::LogFolder`) para aproveitar o gerenciamento de arquivos de log implementado pela [!DNL Platform Server] (consulte `PS::LogDays`).

>[!NOTE]
>
>A nova pasta deve ser criada antes de alterar essa configuração. Verifique se as permissões de acesso estão definidas para que o Serviço de imagem tenha os privilégios de criação, leitura e gravação necessários.

## IS:TraceClient - Nível de Log de Depuração do Servidor de Imagens {#section-3851f1f68e404430985c629ac80534db}

O nível de log pode ser 1, 2, 3 ou 4 (o padrão é 2)

O Nível 1 registra os eventos relacionados à inicialização, ao desligamento e [!DNL Platform Server] conexões.

O Nível 2 também registra a conexão e a desconexão das imagens de origem.

O Nível 3 adiciona o registro de solicitações de dados de pixel e a entrega do mesmo ao [!DNL Platform Server].

O Nível 4 registra todas as mensagens recebidas do [!DNL Platform Server].

Os Níveis 3 e 4 devem ser usados apenas para fins de depuração, pois os arquivos de log podem se tornar muito grandes.

## IS::TraceStatsInterval - Intervalo de Log de Estatísticas do Servidor de Imagem {#section-1d8df96d61044e33a5b2b2b0309c2d59}

O Servidor de Imagens grava estatísticas de memória em seu arquivo de log de rastreamento no intervalo especificado por essa configuração. O intervalo válido é de 5 a 86.400 segundos.
