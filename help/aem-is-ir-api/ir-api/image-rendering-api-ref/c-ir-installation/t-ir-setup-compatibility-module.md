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
1. Copie o conteúdo de [!DNL ir] no diretório [!DNL `ROOT`] diretório.
1. Abertura [!DNL `ROOT/WEB-INF/web.xml`] em um editor de texto.
1. Pesquisar a linha `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Remova o comentário de `<servlet>` e `<servlet-mapping>` específicos.
1. Restart `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Exemplo de Linux®**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

Em seguida, editar [!DNL `web.xml`] usar seu editor favorito para remover o comentário de `<servlet>` e `<servlet-mapping>` específicos.

**Exemplo do Windows**

Abra o Explorer e vá para `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Selecionar todos os arquivos e pastas e copiá-los `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Em seguida, edite o arquivo `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`, sem comentar o `<servlet>` e `<servlet-mapping>` específicos.
