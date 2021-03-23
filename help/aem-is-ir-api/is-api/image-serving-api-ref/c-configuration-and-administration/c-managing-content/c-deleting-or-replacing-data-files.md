---
description: Embora a adição de novos arquivos de dados seja simples e direta, é necessário ter cuidado especial ao substituir arquivos de dados existentes que são usados ativamente pelo servidor. Em vez de simplesmente substituir esses arquivos, é recomendável dar um novo nome ao arquivo de substituição (por exemplo, anexar um sufixo de versão ao nome do arquivo). Depois que o novo arquivo for ativado, a versão antiga poderá ser excluída.
seo-description: Embora a adição de novos arquivos de dados seja simples e direta, é necessário ter cuidado especial ao substituir arquivos de dados existentes que são usados ativamente pelo servidor. Em vez de simplesmente substituir esses arquivos, é recomendável dar um novo nome ao arquivo de substituição (por exemplo, anexar um sufixo de versão ao nome do arquivo). Depois que o novo arquivo for ativado, a versão antiga poderá ser excluída.
seo-title: Exclusão ou substituição de arquivos de dados
solution: Experience Manager
title: Exclusão ou substituição de arquivos de dados
uuid: 7b446144-48f6-4b50-93ec-0287425d932a
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---


# Exclusão ou substituição de arquivos de dados{#deleting-or-replacing-data-files}

Embora a adição de novos arquivos de dados seja simples e direta, é necessário ter cuidado especial ao substituir arquivos de dados existentes que são usados ativamente pelo servidor. Em vez de simplesmente substituir esses arquivos, é recomendável dar um novo nome ao arquivo de substituição (por exemplo, anexar um sufixo de versão ao nome do arquivo). Depois que o novo arquivo for ativado, a versão antiga poderá ser excluída.

>[!NOTE]
>
>Os arquivos de dados nunca devem ser substituídos ou excluídos enquanto estiverem em uso ativo pelo Serviço de imagem. Caso contrário, podem ocorrer erros ou mesmo falhas no servidor.

Em todos os casos, lembre-se de que o cache do Platform Server e as entradas do cache do cliente devem se tornar obsoletos antes que os dados atualizados sejam vistos pelo cliente. Entradas específicas do cache podem ser atualizadas imediatamente usando o comando `cache=validate`.

As alterações nos arquivos de fonte e nos arquivos de perfil ICC não são rastreadas diretamente pelo gerenciador de cache. Se esse recurso for modificado sem alterar sua id, o cache do servidor não saberá sobre a alteração e `cache=validate` não fará com que a entrada do cache seja atualizada. `cache=update` pode ser usada para forçar a regeneração dessas entradas de cache.

Para evitar as complicações da substituição de arquivos, é recomendável dar um novo nome a um arquivo de substituição e atualizar as entradas de catálogo correspondentes. Isso permitirá a substituição de qualquer arquivo de dados enquanto o servidor estiver ativo e fará com que as entradas de cache do servidor fiquem obsoletas imediatamente sem nenhuma intervenção adicional. Essa abordagem pode ser usada para perfis ICC, fontes e todas as imagens gerenciadas por catálogos de imagens.
