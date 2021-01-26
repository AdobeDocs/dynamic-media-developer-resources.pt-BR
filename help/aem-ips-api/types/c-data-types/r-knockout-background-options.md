---
description: Mascarar (separação) o plano de fundo das imagens selecionadas. Isso permite que você as sobreponha em outras camadas com uma transparência fora da imagem do assunto. Um parâmetro opcional que está desativado por padrão.
seo-description: Mascarar (separação) o plano de fundo das imagens selecionadas. Isso permite que você as sobreponha em outras camadas com uma transparência fora da imagem do assunto. Um parâmetro opcional que está desativado por padrão.
seo-title: OpçõesDePlanoDeFundoDeConhecimento
solution: Experience Manager
title: OpçõesDePlanoDeFundoDeConhecimento
topic: Dynamic Media Image Production System API
uuid: 1486d646-f42a-4ed4-9450-313950969c39
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---


# OpçõesDePlanoDeFundo{#knockoutbackgroundoptions}

Mascarar (separação) o plano de fundo das imagens selecionadas. Isso permite que você as sobreponha em outras camadas com uma transparência fora da imagem do assunto. Um parâmetro opcional que está desativado por padrão.

`KnockoutBackgroundOptions=[corner, tolerance, fill]`

## Parâmetros {#section-3149b49ccb714e6eafa6655354816819}

<table id="table_68131DE0A3C84908A43C6F7777F20973"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> canto</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Seleciona o canto com o qual deseja trabalhar. <span class="codeph"> </span> corneraceite estes valores: 
    <ul id="ul_36C2F07706764A7081010D5521BF3096">
     <li id="li_CBACE5C6AA8C48D3BEE033D3AE03AF3C"><span class="codeph"> UpperLeft</span></li>
     <li id="li_49AC53536B4B4D2CA3DD89E2A2B2E95D"><span class="codeph"> Inferior esquerdo</span></li>
     <li id="li_7AD372FF4A9B48F0A16964EE9CB3EE88"><span class="codeph"> UpperRight</span></li>
     <li id="li_D31476DD9A8E4BDBB13A6DDA46547877"><span class="codeph"> Inferior direito</span></li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tolerância</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:duplo</span> </td> 
   <td colname="col3">Uma configuração opcional que remove o espaço em branco das bordas da imagem com base na transparência. Aceita um intervalo de valores de 0,0 a 1,0. Especificar: 
    <ul id="ul_FE5423B857AE43FCBA7A9AEA76C754CC">
     <li id="li_01E3BD0AB8DA4C408B47CB02B269404A">0 para corresponder as cores exatamente. </li>
     <li id="li_FCE21384265D4ECE9C0D785F1BB32C3A">1 para ativar a maioria das diferenças de cor. </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fillMethod</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Controle a transparência de pixels no local especificado pela variável <span class="codeph"><span class="varname"> corner</span></span>. O <span class="codeph"> fillMethod</span> aceita estes valores: </p> 
    <ul id="ul_D95F3B613D344BB89487ED09D83F9217"> 
     <li id="li_3D7B7CA1B9094D16A98E0BA3D962E97F"> <span class="codeph"> FloodFill</span>: Torna transparentes todos os pixels no canto especificado. </li> 
     <li id="li_F97343C3DA7644BCBD1748AD8F9DCE2E"> <span class="codeph"> MatchPixel</span>: Torna todos os pixels correspondentes transparentes, independentemente da localização. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section-3f9edfff321a4e4394f766298b9e284d}

```
<complexType name="KnockoutBackgroundOptions">
        <sequence>
            <!-- corner one of UpperLeft, BottomLeft, UpperRight, BottomRight -->
            <element name="corner" type="xsd:string" minOccurs="1"/>
            <!-- Tolerance real value between 0.0 and 1.0 -->
            <element name="tolerance" type="xsd:double" minOccurs="0"/>
            <!-- one of FloodFill or MatchPixel is required -->
            <element name="fillMethod" type="xsd:string" minOccurs="1"/>
        </sequence>
    </complexType>
```

## Usado por {#section-28c43baafe85434a9ee9e303ed10569a}

O tipo `KnockoutBackgroundOptions` é usado por:

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

