---
description: Contém configurações do Servidor de imagens.
seo-description: Contém configurações do Servidor de imagens.
seo-title: ImageServerRegistry.xml
solution: Experience Manager
title: ImageServerRegistry.xml
topic: Dynamic Media Image Serving - Image Rendering API
uuid: cc401f75-1eb1-40fe-8308-eaaf9e14f906
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---


# ImageServerRegistry.xml{#imageserverregistry-xml}

Contém configurações do Servidor de imagens.

Ao modificar esse arquivo XML, é necessário ter cuidado para manter uma sintaxe XML válida; caso contrário, o Servidor de imagens pode falhar no start.

Para que as alterações entrem em vigor, reinicie o Servidor de imagens após a edição deste arquivo. Somente os valores de elementos listados abaixo são suportados para modificação. Edite qualquer outro conteúdo deste arquivo somente quando solicitado pelo suporte técnico da Dynamic Media.

>[!NOTE]
>
>Não altere a estrutura de `<imageserverregistry>`, incluindo a ordem dos elementos. Tenha cuidado ao editar esse arquivo; caso contrário, o Servidor de imagens poderá falhar no start.

A seguir, são apresentados os elementos que podem ser alterados. Existem outros elementos que não podem ser alterados. A ordem dos elementos abaixo não reflete a ordem em que devem estar presentes no ficheiro.

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
