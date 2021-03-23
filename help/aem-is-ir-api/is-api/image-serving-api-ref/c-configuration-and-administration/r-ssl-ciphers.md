---
description: A tag Connector em server.xml oferece suporte a um atributo ciphers para limitar as cifras que podem ser escolhidas para uma conexão SSL.
seo-description: A tag Connector em server.xml oferece suporte a um atributo ciphers para limitar as cifras que podem ser escolhidas para uma conexão SSL.
seo-title: Definição de cifras SSL
solution: Experience Manager
title: Definição de cifras SSL
uuid: 9490fb9a-5abb-4f5e-b660-b7af0a5e4b4d
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# Definindo cifras SSL{#defining-ssl-ciphers}

A tag Connector em server.xml oferece suporte a um atributo ciphers para limitar as cifras que podem ser escolhidas para uma conexão SSL.

Por padrão, todas as cifras estão disponíveis. A lista é separada por vírgulas e pode conter qualquer um dos seguintes valores:

`SSL_DHE_DSS_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_DSS_WITH_DES_CBC_SHA`

`SSL_DHE_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_RSA_EXPORT_WITH_RC4_40_MD5`

`SSL_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_WITH_RC4_128_MD5`

`SSL_RSA_WITH_RC4_128_SHA`

`TLS_DHE_DSS_WITH_AES_128_CBC_SHA`

`TLS_DHE_RSA_WITH_AES_128_CBC_SHA`

`TLS_RSA_WITH_AES_128_CBC_SHA`

Se algum dos valores estiver errado, o Tomcat habilitará cada cifra. Portanto, é essencial verificar com uma ferramenta externa após a configuração para ver quais cifras estão realmente habilitadas.

Como exemplo, a seguinte configuração habilitará apenas os conjuntos de cifras de &quot;128 bits&quot; e superiores:

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,SSL_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA,TLS_RSA_WITH_AES_128_CBC_SHA"`
