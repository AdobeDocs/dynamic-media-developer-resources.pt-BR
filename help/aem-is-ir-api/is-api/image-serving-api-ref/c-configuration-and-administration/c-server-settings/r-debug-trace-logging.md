---
description: Use essas configurações do servidor para depurar o registro de rastreamento.
seo-description: Use essas configurações do servidor para depurar o registro de rastreamento.
seo-title: Registro de Debug_trace
solution: Experience Manager
title: Registro de Debug_trace
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 33f1d093-007d-453b-965a-9d701a845954
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---


# Debug_trace logging{#debug-trace-logging}

Use essas configurações do servidor para depurar o registro de rastreamento.

>[!NOTE]
>
>É recomendável configurar todos os arquivos de log a serem gravados na mesma pasta que `TC::directory`. Isso garante que todos os arquivos de log do Servidor de imagens participem da rotação automática do arquivo de log configurada com `TC::maxDays`, o que evitará a possível instabilidade do servidor devido a condições de espaço em disco.

## SV::log - Caminho do Arquivo de Log do Supervisor de Servidor {#section-3697bc480ff646e79cacc2812c55ef26}

Nome da pasta e do arquivo base para arquivos de log do Supervisor do Servidor. O caminho pode ser absoluto ou relativo a *[!DNL install_folder]*. O Supervisor de Servidor anexará um hífen e a data atual ( *[!DNL -yyyy-mm-dd]*) ao nome do arquivo (antes do sufixo do arquivo, se houver). É recomendável enviar todos os arquivos de log para a mesma pasta dos arquivos de log do Platform Server ( `PS::LogFolder`) para aproveitar o gerenciamento de arquivos de log implementado pelo Platform Server ( `PS::LogDays`). O padrão é [!DNL logs/Supervisor.log].

>[!NOTE]
>
>A nova pasta deve ser criada antes de alterar essa configuração. Verifique se as permissões de acesso estão definidas para que o Supervisor de Servidor tenha os privilégios de criação, leitura e gravação necessários.

## SV::tracelevel - Nível de Log de Rastreamento do Supervisor de Servidor {#section-36f8634741da4c618d67aa628b5fe474}

O nível de log pode ser 1, 2, 3 ou 4. O padrão é 2.

## IS::Log - Caminho do Arquivo de Log de Depuração do Servidor de Imagens {#section-73a3f09b77f2446c9f82207b7d8aec39}

Nome da pasta e do arquivo base para os arquivos de log de rastreamento do Servidor de imagens. O caminho pode ser absoluto ou relativo a *[!DNL install_folder]*. O ImageServer anexará um hífen e a data atual ( *[!DNL -yyyy-mm-dd]*) ao nome do arquivo (antes do sufixo do arquivo, se houver). É recomendável enviar arquivos de log do Servidor de Imagens para a mesma pasta dos arquivos de log do Servidor de Plataformas ( `PS::LogFolder`) para aproveitar o gerenciamento de arquivos de log implementado pelo Servidor de Plataformas (consulte `PS::LogDays`).

>[!NOTE]
>
>A nova pasta deve ser criada antes de alterar essa configuração. Verifique se as permissões de acesso estão definidas para que o Serviço de imagem tenha os privilégios necessários de criação, leitura e gravação.

## IS:TraceClient - Nível de Log de Depuração do Servidor de Imagens {#section-3851f1f68e404430985c629ac80534db}

O nível de registro pode ser 1, 2, 3 ou 4 (o padrão é 2)

O Nível 1 registra eventos relacionados a conexões de start, desligamento e Servidor de plataforma.

O Nível 2 também registra a conexão e a desconexão das imagens de origem.

O Nível 3 adiciona o registro de solicitações de dados de pixel e delivery igual ao Servidor da plataforma.

O Nível 4 registra todas as mensagens recebidas do Servidor de plataforma.

Os níveis 3 e 4 devem ser usados apenas para fins de depuração, já que os arquivos de log podem se tornar muito grandes.

## IS::TraceStatsInterval - Intervalo de Log de Estatísticas do Servidor de Imagens {#section-1d8df96d61044e33a5b2b2b0309c2d59}

O Servidor de imagens grava estatísticas de memória em seu arquivo de log de rastreamento no intervalo especificado por essa configuração. O intervalo válido é de 5 a 86.400 segundos.
