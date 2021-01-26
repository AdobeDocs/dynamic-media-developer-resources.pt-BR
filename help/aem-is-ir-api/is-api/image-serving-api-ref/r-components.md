---
description: 'O Serviço de Imagens do Scene 7 consiste nos seguintes componentes '
seo-description: 'O Serviço de Imagens do Scene 7 consiste nos seguintes componentes '
seo-title: Componentes do serviço de imagem
solution: Experience Manager
title: Componentes do serviço de imagem
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 84e04972-32ce-4aca-aae6-d5b8bbe761e6
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---


# Componentes do serviço de imagem{#image-serving-components}

O Serviço de imagem do Scene 7 consiste nos seguintes componentes:

<table id="table_534AF33FE5C4453EACAE0DF35E8E3B63"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Componente </p> </th> 
   <th colname="col2" class="entry"> <p>Descrição </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Supervisor do servidor </p> </td> 
   <td colname="col2"> <p>Executável independente responsável por iniciar, parar e garantir a integridade dos outros componentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>Fornece o ambiente para a maioria dos componentes baseados em Java. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Serviço de Monitoramento/Alerta </p> </td> 
   <td colname="col2"> <p>Aplicativo J2EE. Fornece monitoramento de servidor e alerta por email. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Servidor da plataforma </p> </td> 
   <td colname="col2"> <p>Aplicativo J2EE. Gerencia conexões de clientes, registro, comunicações com outros componentes. Acesso HTTP em <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Serviço de cache </p> </td> 
   <td colname="col2"> <p>Aplicativo J2EE. Gerencia os caches de dados do Servidor de plataforma. Acesso HTTP em /is/cache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Servidor de imagens </p> </td> 
   <td colname="col2"> <p>Executa todas as operações de processamento de imagens e de E/S de arquivos de imagem. Os executáveis de 32 bits e 64 bits estão disponíveis para Linux (somente 32 bits para Windows). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Componente de renderização de texto ATE </p> </td> 
   <td colname="col2"> <p>Uma ou mais instâncias do serviço de renderização de texto podem estar ativas quando as operações <span class="codeph"> textPs=</span> são executadas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Componente de renderização SVG </p> </td> 
   <td colname="col2"> <p>Aplicativo Java independente (não hospedado pelo Tomcat). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Renderização de imagem do Dynamic Media (também conhecido como Servidor de renderização) </p> </td> 
   <td colname="col2"> <p>Requer uma licença separada para ativar. Acesso HTTP em <span class="filepath"> /ir/render</span>. Toda a funcionalidade de renderização de imagem é integrada ao Servidor de plataforma e ao Servidor de imagens, sem componentes executáveis separados. </p> </td> 
  </tr> 
 </tbody> 
</table>

Configurações adicionais são fornecidas pelo catálogo padrão ( [!DNL default.ini]) ou catálogos de imagens específicos (consulte [Catálogos de imagens](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) para obter detalhes).
