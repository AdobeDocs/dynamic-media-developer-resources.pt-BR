---
title: Definir e configurar o módulo de compatibilidade do IR 3.x
description: Instale e configure o módulo de compatibilidade do IR 3.x.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# Definir e configurar o módulo de compatibilidade do IR 3.x{#setup-and-configure-ir-x-compatibility-module}

1. Parar `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Altere para o diretório ImageServer webapps.
1. Copie o conteúdo do diretório [!DNL ir] no diretório [!DNL `ROOT`].
1. Abra [!DNL `ROOT/WEB-INF/web.xml`] em um editor de texto.
1. Pesquisar a linha `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Descomente as marcas `<servlet>` e `<servlet-mapping>`.
1. Reinicie `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Exemplo do Linux®**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

Em seguida, edite [!DNL `web.xml`] usando seu editor favorito para remover o comentário das tags `<servlet>` e `<servlet-mapping>`.

**Exemplo do Windows**

Abra o Explorer e vá para `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Selecione todos os arquivos e pastas e copie-os dentro de `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Em seguida, edite o arquivo `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`, cancelando o comentário das marcas `<servlet>` e `<servlet-mapping>`.
