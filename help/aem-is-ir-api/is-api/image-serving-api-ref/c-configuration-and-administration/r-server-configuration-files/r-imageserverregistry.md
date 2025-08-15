---
description: Contém as definições de configuração do Servidor de imagens.
solution: Experience Manager
title: ImageServerRegistry.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4483c5e8-5123-4d0f-bf9a-4ef8d8cec5a9
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# ImageServerRegistry.xml{#imageserverregistry-xml}

Contém as definições de configuração do Servidor de imagens.

Ao modificar esse arquivo XML, é necessário ter cuidado para manter uma sintaxe XML válida; caso contrário, o Servidor de imagens poderá não ser iniciado.

Para que as alterações entrem em vigor, reinicie o Servidor de imagens após editar esse arquivo. Somente os valores de elemento listados abaixo são suportados para modificação. Edite qualquer outro conteúdo deste arquivo somente quando recomendado pelo suporte técnico do Dynamic Media.

>[!NOTE]
>
>Não altere a estrutura de `<imageserverregistry>`, incluindo a ordem dos elementos. Tenha cuidado ao editar esse arquivo; caso contrário, o Servidor de imagens poderá não ser iniciado.

A seguir estão os elementos que podem ser alterados. Há outros elementos presentes que não devem ser alterados. A ordem dos elementos abaixo não reflete a ordem em que eles devem estar presentes no arquivo.

```
<imageserverregistry>
    <TcpPort> 27345 </TcpPort>    
    <RootPath ./images </RootPath>
    <TempDirectory ./temp </TempDirectory>
    <Log> ./logs/ImageServer.log </Log>
    <TraceClient> 2 </TraceClient>
    <TraceStatsInterval> 600 </TraceStatsInterval>
    <PhysicalMemory> 20 </PhysicalMemory>
    <WorkerThreads> 0 </WorkerThreads>
    <SVGTcpPort> 27346 </SVGTcpPort>
    <MaxRenderRgnPixels> 16 </MaxRenderRgnPixels>
    <MaxSavePixels> 100 </MaxSavePixels>
    <MaxMessageSize> 16 </MaxMessageSize>
    <CacheServerUrl> http://localhost:8080/is/cache/secondary </CacheServerUrl>
    <NumberOfTextServers> 0 </NumberOfTextServers>
    <TextServerTcpPortRange> 27347-27380 </TextServerTcpPortRange>
    <SaveDirectory> ./ </SaveDirectory>
    <RemoteUrlDefaultExpiration> 36000 </RemoteUrlDefaultExpiration>
    <RemoteUrlTimeout> 60 </RemoteUrlTimeout>
    <MaxNonDsfSize> 4 </MaxNonDsfSize>
</imageserverregistry>
```

## Notas {#section-7217f011f69f41e7af4f3983d7776d6f}

Vários elementos `<RootPath>` podem estar presentes (um para cada pasta de arquivo de dados de origem). O Servidor de imagens pesquisa os caminhos raiz na ordem especificada para localizar um arquivo de origem específico.
