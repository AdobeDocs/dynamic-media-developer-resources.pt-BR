---
description: Contém as configurações do Servidor de imagem.
seo-description: Contém as configurações do Servidor de imagem.
seo-title: ImageServerRegistry.xml
solution: Experience Manager
title: ImageServerRegistry.xml
uuid: cc401f75-1eb1-40fe-8308-eaaf9e14f906
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---


# ImageServerRegistry.xml{#imageserverregistry-xml}

Contém as configurações do Servidor de imagem.

Ao modificar esse arquivo XML, é necessário tomar cuidado para manter uma sintaxe XML válida; caso contrário, o Servidor de Imagem poderá não conseguir iniciar.

Para que as alterações entrem em vigor, reinicie o Servidor de Imagens após editar este arquivo. Somente os valores de elemento listados abaixo são suportados para modificação. Edite qualquer outro conteúdo desse arquivo somente quando solicitado pelo suporte técnico da Dynamic Media.

>[!NOTE]
>
>Não altere a estrutura de `<imageserverregistry>`, incluindo a ordem dos elementos. Tenha cuidado ao editar esse arquivo; caso contrário, o Servidor de imagem poderá não ser iniciado.

O exemplo a seguir ilustra quais elementos podem ser alterados. Existem outros elementos que não devem ser alterados. A ordem dos elementos abaixo não reflete a ordem em que devem estar presentes no processo.

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

Vários elementos `<RootPath>` podem estar presentes (um para cada pasta do arquivo de dados de origem). O Image Server pesquisa os caminhos raiz na ordem especificada para localizar um arquivo de origem específico.
