---
description: Utilitário de validação de imagem. Esse utilitário de linha de comando verifica os arquivos de imagem para garantir que eles sejam válidos e possam ser lidos sem dificuldade pelo Serviço de imagem.
solution: Experience Manager
title: validate
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---


# validate{#validate}

Utilitário de validação de imagem. Esse utilitário de linha de comando verifica os arquivos de imagem para garantir que eles sejam válidos e possam ser lidos sem dificuldade pelo Serviço de imagem.

Todos os arquivos de imagem não PTIFF devem passar a validação antes que o arquivo seja disponibilizado para o Image Serving como uma imagem de origem. As imagens PTIFF devem ser validadas após operações de cópia potencialmente não fiáveis.

## Uso {#usage}

` validate *``* [ *``*] [ *`fileTypetionssourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -qualquer  </span> </p> <p>Tipo de arquivo de origem; pelo menos um deve ser especificado (-any permite os mesmos tipos de arquivo de imagem compatíveis com IC). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> opções  </span> </span> </p> </td> 
  <td class="stentry"> <p>Outras opções de comando (veja abaixo). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile  </span> </span> </p> </td> 
  <td class="stentry"> <p> Arquivo de imagem. Nenhuma ou mais, separadas por espaços. </p> </td> 
 </tr> 
</table>

## Retorna {#section-67a7cf7c53144fbb8f24b818f4a10901}

0 se bem-sucedido. Se ocorrer um erro, um valor diferente de zero é retornado e os detalhes do erro são enviados para `stderr`.

## Opções {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList  <span class="varname"> listFile  </span> </span> </p> </td> 
  <td class="stentry"> <p>Especifica um arquivo de texto separado contendo a lista de arquivos de imagem. Um registro por arquivo. Se <span class="codeph"> -fileList </span> for incluído, <span class="varname"> sourceFile </span> não deverá ser especificado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels  </span> </p> </td> 
  <td class="stentry"> <p>Permite a verificação de todo o arquivo de imagem. Por padrão, somente o cabeçalho da imagem é validado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile  </span> </p> </td> 
  <td class="stentry"> <p>Verifica a validade do perfil de cores incorporado. Por padrão, o corpo do perfil não está marcado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent  </span> </p> </td> 
  <td class="stentry"> <p> Rejeita imagens com 16 bits por componente de imagem. Sempre especificado pelo Servidor de Imagens quando ele valida imagens de origem remota. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose  </span> </p> </td> 
  <td class="stentry"> <p> Imprime mais informações se a imagem for inválida. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silencioso  </span> </p> </td> 
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

