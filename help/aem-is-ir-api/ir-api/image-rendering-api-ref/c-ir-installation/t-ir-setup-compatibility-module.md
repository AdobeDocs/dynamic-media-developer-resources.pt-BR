---
description: Você deve configurar e configurar o módulo de compatibilidade IR 3.x.
seo-description: Você deve configurar e configurar o módulo de compatibilidade IR 3.x.
seo-title: Configurar e configurar o módulo de compatibilidade IR 3.x
solution: Experience Manager
title: Configurar e configurar o módulo de compatibilidade IR 3.x
topic: Scene7 Image Serving - Image Rendering API
uuid: 609a6ac9-1a4e-4cca-ab08-aa0f957b0e31
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Configurar e configurar o módulo de compatibilidade IR 3.x{#setup-and-configure-ir-x-compatibility-module}

Você deve configurar e configurar o módulo de compatibilidade IR 3.x.

1. Pare `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Altere para o diretório de aplicativos da Web ImageServer.
1. Copie o conteúdo do [!DNL ir] diretório no [!DNL ROOT] diretório.
1. Abrir [!DNL ROOT/WEB-INF/web.xml] em um editor de texto.
1. Procurar a linha `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Exclua os comentários das tags `<servlet>` e `<servlet-mapping>` .
1. Reinicie `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
>**Exemplo de Linux**
>
>`cd /usr/local/scene7/ImageServing/webapps/ROOT`
>
>`cp -r ../ir/* ./`
>
>`cd WEB-INF`
>
>Em seguida, edite [!DNL web.xml]usando seu editor favorito para excluir as `<servlet>` tags e `<servlet-mapping>` .
>
>**Exemplo do Windows**
>
>Abra o Explorer e vá para [!DNL C:\Program Files\Scene7\ImageServing\webapps\ir].
>
>Selecione todos os arquivos e pastas e copie-os dentro [!DNL C:\Program Files\Scene7\ImageServing\webapps\ROOT].
>
>Em seguida, edite o arquivo [!DNL c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml], removendo os comentários das tags `<servlet>` e `<servlet-mapping>` .

