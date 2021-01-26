---
description: Utilitário de validação de imagem. Este utilitário de linha de comando verifica os arquivos de imagem para garantir que eles sejam válidos e possam ser lidos sem dificuldade pelo Serviço de imagem.
seo-description: Utilitário de validação de imagem. Este utilitário de linha de comando verifica os arquivos de imagem para garantir que eles sejam válidos e possam ser lidos sem dificuldade pelo Serviço de imagem.
seo-title: validate
solution: Experience Manager
title: validate
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 87a129ed-950a-4b1a-9240-bf567cd8e38f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---


# validate{#validate}

Utilitário de validação de imagem. Este utilitário de linha de comando verifica os arquivos de imagem para garantir que eles sejam válidos e possam ser lidos sem dificuldade pelo Serviço de imagem.

Todos os arquivos de imagem não PTIFF devem passar a validação antes que o arquivo seja disponibilizado para o Serviço de imagem como uma imagem de origem. As imagens PTIFF devem ser validadas após operações de cópia potencialmente não confiáveis.

## Uso {#usage}

` validate *``* [ *``*] [ *`fileTypetionssourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -qualquer  </span> </p> <p>Tipo de arquivo de origem; pelo menos um deve ser especificado (-any permite os mesmos tipos de arquivos de imagem suportados pelo IC). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> opções  </span> </span> </p> </td> 
  <td class="stentry"> <p>Outras opções de comando (consulte abaixo). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile  </span> </span> </p> </td> 
  <td class="stentry"> <p> Arquivo de imagem. Nenhuma ou mais, separadas por espaços. </p> </td> 
 </tr> 
</table>

## Retorna {#section-67a7cf7c53144fbb8f24b818f4a10901}

0 se bem-sucedido. Se ocorrer um erro, um valor diferente de zero será retornado e os detalhes do erro serão enviados para `stderr`.

## Opções {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList  <span class="varname"> listFile  </span> </span> </p> </td> 
  <td class="stentry"> <p>Especifica um arquivo de texto separado que contém a lista de arquivos de imagem. Um registro por arquivo. Se <span class="codeph"> -fileList </span> estiver incluído, <span class="varname"> sourceFile </span> não deverá ser especificado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels  </span> </p> </td> 
  <td class="stentry"> <p>Permite a verificação de todo o arquivo de imagem. Por padrão, somente o cabeçalho da imagem é validado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile  </span> </p> </td> 
  <td class="stentry"> <p>Verifica a validade do perfil de cor incorporado. Por padrão, o corpo do perfil não está marcado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -cancel16BitPerComponent  </span> </p> </td> 
  <td class="stentry"> <p> Rejeita imagens com 16 bits por componente de imagem. Sempre especificado pelo Servidor de imagens quando ele valida imagens de origem remota. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose  </span> </p> </td> 
  <td class="stentry"> <p> Imprime mais informações se a imagem for inválida. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silent  </span> </p> </td> 
  <td class="stentry"> <p>Desativa a saída <span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span>. Somente um status é retornado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError  </span> </p> </td> 
  <td class="stentry"> <p>Encerra o processamento quando ocorre uma falha de validação de arquivo, mesmo se arquivos adicionais ainda não tiverem sido validados. Por padrão, o processamento continua quando ocorre um erro de validação </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version  </span> </p> </td> 
  <td class="stentry"> <p>Retorna as informações de versão deste utilitário. Especifique sem outras opções. </p> </td> 
 </tr> 
</table>

