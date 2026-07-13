---
description: As definições de configuração de Renderização de Imagem são armazenadas no arquivo de configuração  [!DNL Platform Server] .
solution: Experience Manager
title: Arquivos de configuração
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 44ffebae-4933-455b-a902-4f6e7bb69184
TQID: 'https://experienceleague.adobe.com/KTBXtuSOstPMi7bPQg70jyUVCqcXlLiLPiFFhyp9iFg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 122
ht-degree: 0%

---

# Arquivos de configuração{#configuration-files}

As definições de configuração de Renderização de Imagem são armazenadas no arquivo de configuração [!DNL Platform Server].

O arquivo de configuração do Platform Server está localizado em [!DNL *[!DNL install_root]*/ImageServing/conf/PlatformServer.conf]. Este arquivo é um arquivo de propriedades JAVA. Tenha cuidado ao seguir as convenções apropriadas; caso contrário, [!DNL Platform Server] pode falhar ao iniciar. Uma barra invertida dupla (`\\`) ou uma única barra invertida (/) deve ser usada em vez de uma barra invertida simples (\) nos caminhos de arquivo do Windows, porque a barra invertida é usada como um caractere de escape neste tipo de arquivo. O arquivo contém propriedades não documentadas, que são para uso interno do servidor e não devem ser modificadas.

Consulte a [Referência das Configurações](../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-configuration-settings-reference.md#concept-6947a512d4c94e9fb8a71b80243fee81) para obter uma lista de todas as configurações de Renderização de Imagem.

