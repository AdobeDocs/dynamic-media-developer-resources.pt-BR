---
title: Componentes do Servidor de imagens
description: O Dynamic Media Image Serving consiste nos seguintes componentes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67dd37f3-b11e-42d6-b308-7c1e76a8f2a9
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---

# Componentes do Servidor de imagens{#image-serving-components}

O Dynamic Media Image Serving consiste nos seguintes componentes:

<table id="table_534AF33FE5C4453EACAE0DF35E8E3B63"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Componente </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Supervisor de Servidor </p> </td> 
   <td colname="col2"> <p>Um executável independente responsável por iniciar, parar e garantir a integridade dos outros componentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>Ele fornece o ambiente para a maioria dos componentes baseados em Java. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Serviço de monitoramento/alerta </p> </td> 
   <td colname="col2"> <p>aplicativo J2EE. Fornece monitoramento do servidor e alerta por email. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>[!DNL Platform Server] </p> </td> 
   <td colname="col2"> <p>aplicativo J2EE. Gerencia conexões de clientes, registro, comunicações com outros componentes. Acesso HTTP em <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Serviço de cache </p> </td> 
   <td colname="col2"> <p>aplicativo J2EE. Gerencia os caches de dados de [!DNL Platform Server]. Acesso HTTP em /is/cache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Servidor de imagens </p> </td> 
   <td colname="col2"> <p>Ele executa todas as operações de processamento de imagens e de E/S de arquivos de imagem. Os executáveis de 32 e 64 bits estão disponíveis para Linux® (32 bits somente para Windows). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Componente de renderização de texto ATE </p> </td> 
   <td colname="col2"> <p>Uma ou mais instâncias do serviço de renderização de texto podem estar ativas quando <span class="codeph"> textPs=</span> operações são executadas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Componente de renderização do SVG </p> </td> 
   <td colname="col2"> <p>Aplicativo Java™ independente (não hospedado pelo Tomcat). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Renderização de imagem do Dynamic Media (também conhecido como. Servidor de renderização) </p> </td> 
   <td colname="col2"> <p>Ela requer uma licença separada para ser ativada. Acesso HTTP em <span class="filepath"> /ir/render</span>. Toda a funcionalidade de Renderização de Imagem está integrada ao [!DNL Platform Server] e ao Servidor de Imagens, sem componentes executáveis separados. </p> </td> 
  </tr> 
 </tbody> 
</table>

Configurações adicionais são fornecidas pelo catálogo padrão ( [!DNL default.ini]) ou por catálogos de imagens específicos (consulte [Catálogos de imagens](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) para obter detalhes).
