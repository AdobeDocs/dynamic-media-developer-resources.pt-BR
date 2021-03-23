---
description: Aplicar opções de trabalho em PDF. Um arquivo de opções de tarefa ou uma predefinição de PDF é um arquivo gerado pelo Illustrator na caixa de diálogo de opções Salvar como PDF ou nas predefinições de PDF no InDesign.
seo-description: Aplicar opções de trabalho em PDF. Um arquivo de opções de tarefa ou uma predefinição de PDF é um arquivo gerado pelo Illustrator na caixa de diálogo de opções Salvar como PDF ou nas predefinições de PDF no InDesign.
seo-title: trabalho
solution: Experience Manager
title: trabalho
uuid: 7288cf29-850f-4121-8425-5f995daac22d
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---


# joboption{#joboption}

Aplicar opções de trabalho em PDF. Um arquivo de opções de tarefa ou uma predefinição de PDF é um arquivo gerado pelo Illustrator na caixa de diálogo de opções Salvar como PDF ou nas predefinições de PDF no InDesign.

` joboption= *`value`*`

<table id="simpletable_BA7B58BE0B0740298D45DDEBE7832D93"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> value</span></span> </p> </td> 
  <td class="stentry"> <p>O IPSID do arquivo de opções de trabalho. </p></td> 
 </tr> 
</table>

O arquivo de opções de trabalho pode ser carregado e publicado pelo IPS / Dynamic Media Classic. As opções de PDF contidas no arquivo de opções de trabalho são usadas quando o PDF é gerado.

Atualmente, as seguintes opções são compatíveis:

<table id="simpletable_7E0AE8A06AE54A02AF0107FBEDF73D61"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Geral </p></td> 
  <td class="stentry"> <p> Compatibilidade </p> <p> Compactação no nível do objeto </p> <p> Incorporar miniaturas </p> <p> Otimizar para exibição rápida da Web </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Imagens </p></td> 
  <td class="stentry"> <p> Reduza a amostra, a resolução, o limite e a compactação para cor, cinza e mono </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Fontes </p></td> 
  <td class="stentry"> <p> Incorporar todas as fontes </p> <p> Incorporar fontes OpenType </p> <p> Subconjunto de fontes incorporadas quando a porcentagem de caracteres usados for menor que: </p> <p> Sempre Incorporar Lista </p> <p> Lista Nunca Incorporar </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Cor </p></td> 
  <td class="stentry"> <p> Estratégia de cor (Somente imagens de tag são tratadas como tags de tudo) </p> <p> Propósito de renderização do documento </p> <p> Somente os seguintes espaços de trabalho são compatíveis com a 4.2.5. </p> <p> 
    <ul id="ul_3F3EFDFB6A3340978AE31DEDF0FDA2C8"> 
     <li id="li_17A9FA99D6CA4C5182E383A85F0E3C90"> RGB <p> 
       <ul id="ul_1DD0C264DA1248319E751ADD18140C6D"> 
        <li id="li_B91B4D0C1D80442EB8690933AFA1F093"> e-sRGB </li> 
        <li id="li_D7F8C500DF5E4CBC8FFA4FEFB8E4E036"> scRGB com intervalo de codificação [-4.0, 4.0] </li> 
        <li id="li_942CD69732984E16A71C2F75EC5B5245"> Lab D50 </li> 
        <li id="li_7063B9E98D1E4946AC8F0EF7BC988806"> PCS XYZ </li> 
        <li id="li_5809447576B147B68630C4B7EC2E7870"> XYZ plana </li> 
        <li id="li_3B5DA42A04124A6BAA12343AFC19F620">ROMM-RGB linear </li> 
        <li id="li_DEC3028FA9C34176B761D12B7179B44F">ROMM-RGB </li> 
        <li id="li_3E7E7C4A680C4E3EADE0A26048ECF1F4"> sYCC de 8 bits </li> 
        <li id="li_16A615C9A74D443AB3C63B3FE3AB5443"> e-sYCC de 8 bits </li> 
       </ul> </p> </li> 
     <li id="li_AFA6D4D8C0624AA495E2EB2F0F0C7F7B">Cinza <p> 
       <ul id="ul_945389DD426F44C09EB9C7F23933CB77"> 
        <li id="li_DB0AE3DFFC184480BB91666FF1BB4776">Gama cinza 1.8 </li> 
        <li id="li_755C556ED94740D1BD30EBE67018E074">Gama cinza 2.2 </li> 
        <li id="li_67437440AFB54B7686333A55233AA87F">Ganho de Ponto 10% </li> 
        <li id="li_0D6CA6004EC84048B5F2198406F4F343">Ganho de Ponto 15% </li> 
        <li id="li_1AFD11C23AB147978559D8F00BFB3142">Ganho de Ponto 20% </li> 
        <li id="li_6CD5ACEF6B0B49E8BACA8264FE0E9C44"> Ganho de Ponto 25% </li> 
        <li id="li_AB5F1FA7111041BD82353E02A284A546">Ganho de Ponto 30% </li> 
        <li id="li_7433278AE8054AD28BD38A0A6E4EF7EF"> Cinza </li> 
       </ul> </p> </li> 
    </ul> </p> <p> Preservar valores CMYK para espaços de cores CMYK calibrados </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Avançado </p></td> 
  <td class="stentry"> <p>Preservar comentários OPI é sempre ativado. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Padrões </p></td> 
  <td class="stentry"> <p>Padrão de conformidade. </p></td> 
 </tr> 
</table>

