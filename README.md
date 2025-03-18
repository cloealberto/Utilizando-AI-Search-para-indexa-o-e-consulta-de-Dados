# Azure Cognitive Search - Passo a Passo no Portal do Azure

## Introdução
O **Azure Cognitive Search** é uma plataforma de busca que permite realizar pesquisas poderosas sobre grandes volumes de dados não estruturados. Ele utiliza a interface gráfica do portal do Azure para facilitar a configuração e gerenciamento de buscas, sem a necessidade de escrever código.

Este tutorial irá guiá-lo a criar e configurar um serviço de pesquisa no Azure, utilizando apenas a interface gráfica, para que você possa realizar consultas e explorar os dados indexados de forma eficiente.

## 1. Criar o Serviço de Pesquisa

1. Acesse o portal do [Azure](https://portal.azure.com/) com sua conta Microsoft.
2. No menu à esquerda, clique em **Criar um recurso**.
3. Na barra de pesquisa, digite **Azure Cognitive Search** e selecione a opção **Azure Cognitive Search**.
4. Clique em **Criar**.
5. Preencha as informações necessárias:
   - **Assinatura**: Escolha a assinatura que deseja usar.
   - **Grupo de Recursos**: Crie um novo grupo de recursos ou selecione um existente.
   - **Nome do Serviço de Pesquisa**: Escolha um nome único para o seu serviço.
   - **Região**: Escolha a região mais próxima de você.
   - **Plano de Preço**: Escolha o plano adequado (se estiver começando, o **Free** é suficiente).
6. Clique em **Revisar + criar** e depois em **Criar**.

Aguarde alguns minutos enquanto o serviço é provisionado. Quando estiver pronto, você será redirecionado para a página do seu serviço de pesquisa.

## 2. Criar um Índice de Pesquisa

Agora que o serviço de pesquisa está pronto, você pode criar um índice para armazenar os dados.

1. No painel do serviço de pesquisa, clique em **Índices** na barra lateral esquerda.
2. Clique em **+ Novo índice**.
3. Defina os campos do índice. Um índice pode ter diversos campos como **id**, **nome**, **descrição**, etc.
   - Clique em **Adicionar Campo**.
   - Preencha os campos desejados com as propriedades de cada campo (ex: **id** (chave primária), **nome** (string), **preço** (decimal)).
   - Marque a opção **pesquisável** em campos que você quer que sejam incluídos nas buscas.
4. Clique em **Salvar** para criar o índice.

## 3. Carregar Dados no Índice

Agora, vamos carregar dados para o índice, para que você possa realizar buscas.

1. No painel do índice, clique em **Fontes de Dados** e depois em **+ Nova Fonte de Dados**.
2. Escolha a **Fonte de Dados** de onde deseja carregar os dados:
   - **Blob Storage**: Para dados em arquivos no Azure Storage.
   - **SQL Database**: Para dados armazenados em um banco de dados SQL.
3. Preencha as informações de conexão para a fonte de dados escolhida.
4. Clique em **Validar** para garantir que a fonte de dados está acessível e, em seguida, em **Salvar**.
   
## 4. Criar um Plano de Indexação

1. Após adicionar a fonte de dados, vá para a seção **Indexadores**.
2. Clique em **+ Novo Indexador**.
3. Escolha a **Fonte de Dados** que você configurou no passo anterior.
4. Selecione o **Índice** que você criou e configure como os dados devem ser indexados.
5. Clique em **Salvar**. O indexador irá processar os dados e preencher o índice com as informações.

## 5. Realizar Consultas de Pesquisa

Agora que o índice está preenchido com dados, você pode fazer consultas diretamente no portal do Azure:

1. No painel do serviço de pesquisa, clique em **Explorador de Pesquisa**.
2. Selecione o índice que você deseja consultar.
3. Na caixa de pesquisa, insira o termo que deseja buscar.
4. O portal exibirá os resultados da pesquisa, com base nos dados indexados.

## 6. Insights e Possibilidades de Ferramentas

O Azure Cognitive Search pode ser utilizado em diversos cenários, como:

- **E-commerce**: Para criar uma busca rápida e precisa de produtos, facilitando a navegação de usuários.
- **Blogs e Sites de Conteúdo**: Permite a pesquisa eficiente de artigos, postagens e outras informações.
- **Sistemas de Análise de Dados**: Pode ser usado em plataformas de análise de dados para procurar insights de grandes volumes de dados estruturados e não estruturados.

## 7. Aprendizados Adquiridos

Durante o desenvolvimento deste projeto, aprendi a:
- Criar e configurar um serviço de pesquisa no Azure.
- Definir índices de pesquisa de acordo com as necessidades do negócio.
- Utilizar o portal do Azure para gerenciar dados, fontes e consultas de forma prática.
- Explorar as diversas funcionalidades do Azure Cognitive Search, como indexação incremental e busca avançada.
