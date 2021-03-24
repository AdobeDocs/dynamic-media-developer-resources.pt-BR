---
description: Define a senha de um usuário específico ou padrão para um valor específico, dependendo de você especificar um identificador de usuário.
solution: Experience Manager
title: setPassword
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---


# setPassword{#setpassword}

Define a senha de um usuário específico ou padrão para um valor específico, dependendo de você especificar um identificador de usuário.

A data de expiração da senha é opcional. Se omitida, a senha nunca expirará.

## Tipos de usuário autorizados {#section-39ae61d78cab4492a6efc1fc0d2f06c4}

>[!NOTE]
>
>** Somente o tipo de  `IpsAdmin` usuário está autorizado a executar chamadas setPassword para outros usuários.

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`

## Parâmetros {#section-0531294341f7483d89dacaa393dd659a}

**Entrada (setPasswordParam)**

<table id="table_BF54512811344E0B979C5070354E8048"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obrigatório </p> </th> 
   <th colname="col4" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> userHandle  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Identificador do usuário. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> senha  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>Sim </p> </td> 
   <td colname="col4"> <p>Senha. </p> <p>Os seguintes requisitos são aplicados na senha escolhida: </p> <p> 
     <ul id="ul_E5BE3621127C476788412174584075B3"> 
      <li id="li_0132852AFD774659A0224C450F19418C">As senhas fazem distinção entre maiúsculas e minúsculas. </li> 
      <li id="li_71224B3A89C8461AB689BAD383EC8CEA">O comprimento mínimo da senha é de oito caracteres. </li> 
      <li id="li_C21B6843EA734D1ABE0580185F775408">A senha deve conter um ou mais caracteres das seguintes classes de caracteres: 
       <ul id="ul_D5D3911AD6214035BBD2AB8350A459C7"> 
        <li id="li_6E3F084100104F2CBCF130EF8852C7B7">Caracteres em inglês minúsculos. Por exemplo, <span class="codeph"> a b c d e </span> e assim por diante </li> 
        <li id="li_1FDED8D7348842BC857320D797D41217">Caracteres em inglês maiúsculos. Por exemplo, <span class="codeph"> A B C D E </span> e assim por diante. </li> 
        <li id="li_C3C4D5412AA749F3B78F37B2B696CF80">Números. Por exemplo, <span class="codeph"> 1 2 3 4 5 </span> e assim por diante. </li> 
        <li id="li_2730798F26E74B878BEDE510CD06D8DD">Caracteres de símbolo especial. Por exemplo, você pode usar qualquer um dos seguintes: <span class="codeph"> ` ~ ! @ # $ % ^ * ( ) _ + - = { } | [ ] &amp; \ : " ; " &lt; &gt; ? , . / </span> </li> 
       </ul> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> passwordExpires  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:dateTime  </span> </p> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Determina a data de expiração da senha. <p>Observação:  Forneça o fuso horário com a solicitação para esse campo. Os fusos horários são ajustados para Hora central. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Saída (setPasswordReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-23a6fbabdb3c4c3180076057e47ae567}

Este exemplo de código cria uma senha de usuário. A senha nunca expira porque `passwordExpires` foi omitida.

**Solicitação**

```java
<ns1:setPasswordParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">  
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle> 
   <ns1:password>@Do6e$ySt3mz</ns1:password> 
</ns1:setPasswordParam>
```

**Resposta**

Nenhum.
