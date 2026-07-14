---
description: Um usuário de recursos e tipos no sistema.
solution: Experience Manager
title: Usuário
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
TQID: 'https://experienceleague.adobe.com/XM-2FjVie-j71W3Sc3-TypNJUFnz5AQuZZuGOx1fePs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 0%

---

# [!DNL User]{#user}

Um usuário de recursos e tipos no sistema.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| userHandle | `xsd:string` | Identificador de usuário. |
| firstName | `xsd:string` | Nome do usuário. |
| lastName | `xsd:string` | Sobrenome do usuário. |
| email | `xsd:string` | endereço de e-mail. |
| defaultRole | `xsd:string` | Define a função de um usuário em cada empresa à qual ele pertence. No entanto, a função de usuário `IpsAmin` substitui outras funções de usuário. |
| isValid | `xsd:boolean` | Determina se o usuário é válido. |
| passwordExpires | `xsd:dateTime` | Define a data de expiração da senha. |

