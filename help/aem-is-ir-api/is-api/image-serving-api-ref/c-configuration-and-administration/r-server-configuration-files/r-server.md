---
description: Contém configurações do servidor da plataforma.
seo-description: Contém configurações do servidor da plataforma.
seo-title: server.xml
solution: Experience Manager
title: server.xml
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6f8b7047-6de6-4a56-96b7-58c481150e32
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---


# server.xml{#server-xml}

Contém configurações do servidor da plataforma.

Ao modificar esse arquivo XML, é necessário ter cuidado para manter uma sintaxe XML válida; caso contrário, o Servidor de plataforma pode falhar no start.

Para que as alterações entrem em vigor, o Servidor de plataforma deve ser reiniciado após a edição desse arquivo.

O diagrama a seguir ilustra quais configurações podem ser alteradas neste arquivo. Consulte as seções correspondentes mais cedo neste documento para obter uma descrição dessas configurações. Observe que este diagrama não é uma representação completa de [!DNL server.xml].

```
<Server>
   <Service name="Catalina">
     <Connector port="TC::PsPort" />
     <Connector port="TC::SslPort"
        keystoreFile="TC::keystoreFile"
        keystoreType="TC::keystoreType"
        keystorePass="TC::keystorePass" 
        scheme="https" secure="true" URIEncoding="UTF-8" />
     <Engine>
        <Valve directory="TC::directory" 
           maxDays="TC::maxDays" 
           prefix="TC::prefix" 
           pattern="TC::pattern" 
     </Engine>  
   </Service>
</Server>
```

