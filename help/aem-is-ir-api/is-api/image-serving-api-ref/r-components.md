---
description: 'O Scene 7 Image Serving consiste nos seguintes componentes '
solution: Experience Manager
title: Componentes do Image Serving
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---


# Componentes de disponibilização de imagens{#image-serving-components}

O Scene 7 Image Serving consiste nos seguintes componentes:

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
   <td colname="col2"> <p>Executável autônomo responsável por iniciar, parar e garantir a integridade dos outros componentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>Fornece o ambiente para a maioria dos componentes baseados em Java. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Serviço de Monitoramento/Alerta </p> </td> 
   <td colname="col2"> <p>Aplicativo J2EE. Fornece monitoramento de servidor e alertas de email. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Servidor da plataforma </p> </td> 
   <td colname="col2"> <p>Aplicativo J2EE. Gerencia conexões de clientes, registro, comunicações com outros componentes. Acesso HTTP em <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Serviço de cache </p> </td> 
   <td colname="col2"> <p>Aplicativo J2EE. Gerencia os caches de dados do Servidor de Plataforma. Acesso HTTP em /is/cache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Servidor de imagem </p> </td> 
   <td colname="col2"> <p>Executa todas as operações de processamento de imagens e de E/S de arquivos de imagens. Os executáveis de 32 e 64 bits estão disponíveis para Linux (somente 32 bits para Windows). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Componente de renderização de texto ATE </p> </td> 
   <td colname="col2"> <p>Uma ou mais instâncias do serviço de renderização de texto podem estar ativas quando operações <span class="codeph"> textPs=</span> são executadas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Componente de renderização SVG </p> </td> 
   <td colname="col2"> <p>Aplicativo Java independente (não hospedado pelo Tomcat). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Renderização de imagem do Dynamic Media (também conhecido como Servidor de renderização) </p> </td> 
   <td colname="col2"> <p>Requer uma licença separada para ativar. Acesso HTTP em <span class="filepath"> /ir/render</span>. Toda a funcionalidade Renderização de imagem é integrada ao Servidor de plataforma e ao Servidor de imagem, sem componentes executáveis separados. </p> </td> 
  </tr> 
 </tbody> 
</table>

Configurações adicionais são fornecidas pelo catálogo padrão ( [!DNL default.ini]) ou catálogos de imagem específicos (consulte [Catálogos de imagem](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) para obter detalhes).
