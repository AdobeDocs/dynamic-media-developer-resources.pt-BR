---
description: Configurações que ajudam a melhorar a nitidez da imagem para arquivos TIF de pirâmide otimizados.
solution: Experience Manager
title: OpçõesDeMáscaraSemNitidez
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 7150b4a8-a44d-4858-96f2-6004d5f48e77
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# [!DNL UnsharpMaskOptions]{#unsharpmaskoptions}

Configurações que ajudam a melhorar a nitidez da imagem para arquivos TIF de pirâmide otimizados.

`unsharpMaskOptions=[ *`quantidade, raio, limite, monocromático`*]`

## Parâmetros {#section-c3f0d03136ba4422819cb463bd393885}

Especifique um valor para `unsharpMaskOptions` opções com `minOccurs=" *`n`*".`

<table id="table_D1392963C5694969A9D546F82DB6F45C">
 <thead>
  <tr>
   <th colname="col1" class="entry"> Nome </th>
   <th colname="col2" class="entry"> Tipo </th>
   <th colname="col3" class="entry"> Descrição </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> quantidade</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:duplo</span></td>
   <td colname="col3"><p>Controla o contraste aplicado aos pixels de borda. 
     <ul id="ul_7AA17E354EE64BC4A5BEAE853FF17191">
      <li id="li_42FB21C7ED884E1DB03274130B8DCB10">Intervalo: 0,0 - 5,0 </li>
      <li id="li_E980CAA1A9C54D60A121F21C964820FF">Padrão: 0 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> raio</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:duplo</span></td>
   <td colname="col3"><p>Controla a nitidez definindo o número de pixels em torno da borda de uma imagem. O valor correto depende do tamanho da imagem. 
     <ul id="ul_D4391CD407DE4B48AF4523EBD85D0D40">
      <li id="li_8AEF11A489484EFD91416F8A03C4DB25">Intervalo: 0,0 - 250,0 </li>
      <li id="li_9F1D1B52AFBA46B8BDCDF99A21140002">Valores baixos ajustam a nitidez somente dos pixels da borda. </li>
      <li id="li_7D9FD8AA4899404283D7AB596364A4AF">Valores altos ajustam a nitidez de uma faixa mais ampla de pixels. </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> limite</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>Determina como os pixels devem ser diferentes da área ao redor antes de serem considerados pixels de borda e poderem ser nitidados. 
     <ul id="ul_117E556E3ECF42CC878DD80D338D19CA">
      <li id="li_CFEE76DB78BF437E8463C9089486F8A6">Intervalo: 0 - 255 (somente números inteiros). </li>
      <li id="li_77113DC2698A4D48B11288718766E6A2">Padrão: 6 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> monocromático</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>Os valores incluem somente <span class="codeph"> 0</span> ou <span class="codeph"> 1</span>. </p><p>Defina como <span class="codeph"> 0</span> para aplicar separadamente a cada componente de cor ou como <span class="codeph"> 1</span> para aplicar somente ao brilho da imagem (intensidade). A máscara da camada ou a máscara composta também é afiada. </p><p><span class="codeph"><span class="varname"> monocromático</span></span> é ignorado para imagens em tons de cinza. </p></td>
  </tr>
 </tbody>
</table>

## Exemplo {#section-38adca96c7714cfea35331d20403f59e}

```
<element name="unsharpMaskOptions" type="types:UnsharpMaskOptions" minOccurs="0"/>
    <complexType name="UnsharpMaskOptions">
        <sequence>
            <element name="amount" type="xsd:double" minOccurs="0"/>
            <element name="radius" type="xsd:double" minOccurs="0"/>
            <element name="threshold" type="xsd:int" minOccurs="0"/>
            <element name="monochrome" type="xsd:int" minOccurs="0"/>        
        </sequence>
    </complexType>
```

## Usado por {#section-db8124a5468b498694a780f8a56a4560}

O tipo `unsharpMaskOptions` é usado por:

* [TrabalhoReprocessAssets](../../types/c-data-types/r-reprocess-assets-job.md#reference-a303f7832ae44fdab1dca7cc8bef3fa3)
* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

>[!MORELIKETHIS]
>
>* [Referência da API de disponibilização de imagens: op_usm](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/image-serving-api/http-protocol-reference/command-reference/r-op-usm.html?lang=pt-BR)
