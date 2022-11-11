---
description: Contém as configurações do servidor da plataforma.
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 72b343ba-0d4b-405a-ace3-d44c4d4c44b0
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# server.xml{#server-xml}

Contém as configurações do servidor da plataforma.

Ao modificar esse arquivo XML, é necessário ter cuidado para manter uma sintaxe XML válida, caso contrário, a variável [!DNL Platform Server] pode falhar no início.

Para que as alterações entrem em vigor, a variável [!DNL Platform Server] deve ser reiniciado após a edição deste arquivo.

O diagrama a seguir ilustra quais configurações podem ser alteradas neste arquivo. Consulte as seções correspondentes anteriormente neste documento para obter uma descrição dessas configurações. Observe que esse diagrama não é uma representação completa de [!DNL server.xml].

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
