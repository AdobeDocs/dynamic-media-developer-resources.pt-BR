---
description: A tag Connector em server.xml oferece suporte a um atributo ciphers para limitar os ciphers que podem ser escolhidos para uma conexão SSL.
seo-description: A tag Connector em server.xml oferece suporte a um atributo ciphers para limitar os ciphers que podem ser escolhidos para uma conexão SSL.
seo-title: Definição de cifras SSL
solution: Experience Manager
title: Definição de cifras SSL
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9490fb9a-5abb-4f5e-b660-b7af0a5e4b4d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# Definindo cifras SSL{#defining-ssl-ciphers}

A tag Connector em server.xml oferece suporte a um atributo ciphers para limitar os ciphers que podem ser escolhidos para uma conexão SSL.

Por padrão, todos os cifras estão disponíveis. A lista é separada por vírgulas e pode conter qualquer um dos seguintes valores:

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

Se algum dos valores estiver errado, o Tomcat ativará cada cifra. Portanto, é essencial verificar com uma ferramenta externa após a configuração para ver quais codificadores estão realmente ativados.

A título de exemplo, a configuração a seguir habilitará apenas os conjuntos de criptografia de &quot;128 bits&quot; e acima:

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,SSL_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA,TLS_RSA_WITH_AES_128_CBC_SHA"`
