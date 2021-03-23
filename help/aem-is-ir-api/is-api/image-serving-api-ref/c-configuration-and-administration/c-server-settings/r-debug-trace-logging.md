---
description: Use essas configurações do servidor para depurar o log de rastreamento.
seo-description: Use essas configurações do servidor para depurar o log de rastreamento.
seo-title: Registro do Debug_trace
solution: Experience Manager
title: Registro do Debug_trace
uuid: 33f1d093-007d-453b-965a-9d701a845954
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---


# Registro do Debug_trace{#debug-trace-logging}

Use essas configurações do servidor para depurar o log de rastreamento.

>[!NOTE]
>
>É recomendável configurar todos os arquivos de log a serem gravados na mesma pasta de `TC::directory`. Isso garante que todos os arquivos de log do Servidor de Imagens participem da rotação automática do arquivo de log configurada com `TC::maxDays`, o que impedirá uma possível instabilidade do servidor devido a condições de espaço insuficiente em disco.

## SV::log - Caminho do Arquivo de Log do Supervisor Trace do Servidor {#section-3697bc480ff646e79cacc2812c55ef26}

Nome da pasta e do arquivo base para arquivos de log do Server Supervisor. O caminho pode ser absoluto ou relativo a *[!DNL install_folder]*. O Supervisor de Servidor anexará um hífen e a data atual ( *[!DNL -yyyy-mm-dd]*) ao nome do arquivo (antes do sufixo do arquivo, se houver). É recomendável enviar todos os arquivos de log para a mesma pasta que os arquivos de log do Servidor de Plataforma ( `PS::LogFolder`) para aproveitar o gerenciamento de arquivos de log implementado pelo Servidor de Plataforma ( `PS::LogDays`). O padrão é [!DNL logs/Supervisor.log].

>[!NOTE]
>
>A nova pasta deve ser criada antes de alterar essa configuração. Verifique se as permissões de acesso estão definidas para que o Supervisor de Servidor tenha os privilégios de criação, leitura e gravação necessários.

## SV::tracelevel - Nível de Log de Rastreamento do Supervisor de Servidor {#section-36f8634741da4c618d67aa628b5fe474}

O nível de log pode ser 1, 2, 3 ou 4. O padrão é 2.

## IS::Log - Caminho do Arquivo de Log de Depuração do Servidor de Imagens {#section-73a3f09b77f2446c9f82207b7d8aec39}

Nome da pasta e do arquivo base para os arquivos de log de rastreamento do Servidor de imagens. O caminho pode ser absoluto ou relativo a *[!DNL install_folder]*. O ImageServer anexará um hífen e a data atual ( *[!DNL -yyyy-mm-dd]*) ao nome do arquivo (antes do sufixo do arquivo, se houver). É recomendável enviar arquivos de log do Servidor de Imagem para a mesma pasta que os arquivos de log do Servidor de Plataforma ( `PS::LogFolder`) para aproveitar o gerenciamento de arquivos de log implementado pelo Servidor de Plataforma (consulte `PS::LogDays`).

>[!NOTE]
>
>A nova pasta deve ser criada antes de alterar essa configuração. Verifique se as permissões de acesso estão definidas para que o Serviço de imagem tenha os privilégios de criação, leitura e gravação necessários.

## IS:TraceClient - Nível de Log de Depuração do Servidor de Imagens {#section-3851f1f68e404430985c629ac80534db}

O nível de log pode ser 1, 2, 3 ou 4 (o padrão é 2)

O Nível 1 registra os eventos relacionados às conexões de inicialização, desativação e Servidor da Plataforma.

O Nível 2 também registra a conexão e a desconexão das imagens de origem.

O Nível 3 adiciona o registro de solicitações de dados de pixel e o mesmo ao Servidor de plataforma.

O Nível 4 registra todas as mensagens recebidas do Servidor da Plataforma.

Os Níveis 3 e 4 devem ser usados apenas para fins de depuração, pois os arquivos de log podem se tornar muito grandes.

## IS::TraceStatsInterval - Intervalo de Log de Estatísticas do Servidor de Imagem {#section-1d8df96d61044e33a5b2b2b0309c2d59}

O Servidor de Imagens grava estatísticas de memória em seu arquivo de log de rastreamento no intervalo especificado por essa configuração. O intervalo válido é de 5 a 86.400 segundos.
