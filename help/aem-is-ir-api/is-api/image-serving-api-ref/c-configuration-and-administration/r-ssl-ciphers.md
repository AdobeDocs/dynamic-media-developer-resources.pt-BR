---
description: A tag Connector em server.xml oferece suporte a um atributo ciphers para limitar as cifras que podem ser escolhidas para uma conexão SSL.
solution: Experience Manager
title: Definição de cifras SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 7734ba02-4442-4a3d-acbf-e14d8ad66279
source-git-commit: 370444b85cb2636d109df4e2681e3e078d6f1e1a
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# Definição de cifras SSL{#defining-ssl-ciphers}

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

<!-- WEAK CQDOC-19433 `SSL_RSA_WITH_3DES_EDE_CBC_SHA` -->

`SSL_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_WITH_RC4_128_MD5`

`SSL_RSA_WITH_RC4_128_SHA`

`TLS_DHE_DSS_WITH_AES_128_CBC_SHA`

`TLS_DHE_RSA_WITH_AES_128_CBC_SHA`

<!-- WEAK CQDOC-19433 `TLS_RSA_WITH_AES_128_CBC_SHA` -->

Se algum dos valores estiver errado, o Tomcat habilitará cada cifra. Portanto, é essencial verificar com uma ferramenta externa após a configuração para ver quais cifras estão realmente habilitadas.

Como exemplo, a configuração a seguir ativa apenas os conjuntos de cifras de &quot;128 bits&quot; e superiores:

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA"`
