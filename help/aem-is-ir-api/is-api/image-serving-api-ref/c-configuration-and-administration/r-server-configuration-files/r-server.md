---
description: Contém as configurações do servidor da plataforma.
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin,User
exl-id: 72b343ba-0d4b-405a-ace3-d44c4d4c44b0
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---

# server.xml{#server-xml}

Contém as configurações do servidor da plataforma.

Ao modificar esse arquivo XML, é necessário tomar cuidado para manter uma sintaxe XML válida; caso contrário, o Servidor da Plataforma poderá não conseguir iniciar.

Para que as alterações entrem em vigor, o Servidor de Plataforma deve ser reiniciado após a edição deste arquivo.

O diagrama a seguir ilustra quais configurações podem ser alteradas neste arquivo. Consulte as seções correspondentes anteriormente neste documento para obter uma descrição dessas configurações. Observe que este diagrama não é uma representação completa de [!DNL server.xml].

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
