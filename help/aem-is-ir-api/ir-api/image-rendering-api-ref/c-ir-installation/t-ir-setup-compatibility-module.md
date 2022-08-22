---
title: Configurar e configurar o módulo de compatibilidade IR 3.x
description: Configure o módulo de compatibilidade IR 3.x e configure-o.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Configurar e configurar o módulo de compatibilidade IR 3.x{#setup-and-configure-ir-x-compatibility-module}

1. Stop `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Altere para o diretório de webapps ImageServer.
1. Copie o conteúdo do [!DNL ir] no diretório [!DNL `ROOT`] diretório.
1. Abrir [!DNL `ROOT/WEB-INF/web.xml`] em um editor de texto.
1. Pesquisar a linha `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Exclua o comentário da `<servlet>` e `<servlet-mapping>` tags.
1. Reiniciar `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Exemplo de Linux®**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

Em seguida, edite [!DNL `web.xml`] usando seu editor favorito para remover o comentário `<servlet>` e `<servlet-mapping>` tags.

**Exemplo do Windows**

Abra o Explorer e vá para `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Selecionar todos os arquivos e pastas e copiá-los dentro `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Em seguida, edite o arquivo `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`, descomentando o `<servlet>` e `<servlet-mapping>` tags.
