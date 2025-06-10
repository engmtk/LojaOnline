Descrição Geral do Programa
Este programa é uma aplicação web ASP.NET Core que realiza operações de CRUD (Create, Read, Update, Delete) para gerenciar registros de usuários e produtos em uma loja online. Ele também possui funcionalidades de consulta e rastreamento de interações do usuário, 
registrando todas as ações realizadas no sistema.

O banco de dados utilizado contém informações dos usuários, como CPF/CNPJ, Nome Completo, Código e Nome do Produto, além de informações relacionadas às datas de entrada e saída e ao status de "Encerrado" (se o registro está ativo ou não).
Principais Funcionalidades

1. CRUD (Create, Read, Update, Delete)
O programa permite a manipulação de registros de usuários e produtos através de quatro principais operações:
    Create (Criar):
Permite a inserção de novos registros de usuários no banco de dados, com informações como CPF/CNPJ, Nome, Código e Nome do Produto, Data de Entrada, Data de Saída, e o campo Encerrado.
A ação de criação é registrada em um arquivo de log no formato C:\Login\DDMMAAAALojaOnline.txt.

Read (Ler):
Lista todos os usuários e seus produtos em uma tabela centralizada.
A listagem também permite a consulta por CPF/CNPJ, Nome Completo ou Código do Produto. Quando um termo de pesquisa é fornecido, a listagem exibe apenas os registros correspondentes.
Cada consulta ou visualização da lista de usuários é registrada no log.

Update (Atualizar):
Permite a edição de um registro existente, modificando informações como Nome Completo, Nome do Produto, e Data de Saída, entre outros.
A atualização do registro é registrada no log para rastreamento.

Delete (Deletar):
Permite excluir registros de usuários da base de dados.
A deleção é confirmada por uma tela de confirmação, e o registro excluído é removido permanentemente do banco de dados.
A deleção também é registrada no arquivo de log.

3. Consulta (Pesquisa)

O programa permite a pesquisa por registros com base em CPF/CNPJ, Nome Completo ou Código do Produto.
A consulta é feita através de um campo de pesquisa na página principal. Ao digitar um termo de pesquisa e clicar em "Pesquisar", o sistema filtra os registros de acordo com o critério fornecido.
Toda consulta realizada é registrada no log com o termo de pesquisa utilizado.

4. Sistema de Logging (Rastreamento de Ações)
O programa possui um sistema de logging que grava todas as interações do usuário com o sistema. Ele registra ações como:
Acessos à lista de usuários.
Criação de novos registros.
Edição de registros existentes.
Exclusão de registros.

Consultas realizadas com termos de pesquisa específicos.
Todas as ações são registradas em um arquivo de log localizado no caminho C:\Login\DDMMAAAALojaOnline.txt, com o nome formatado de acordo com a data (dia/mês/ano).

Exemplo de formato do log: yaml

22/09/2024 14:30:45: Usuário criado: CPF/CNPJ 12345678900, Produto 100
22/09/2024 14:32:10: Usuário editado: CPF/CNPJ 12345678900, Produto 100
22/09/2024 14:35:55: Usuário deletado: CPF/CNPJ 12345678900, Produto 100
22/09/2024 14:38:12: Consulta realizada: 'Armazem'

5. Layout Responsivo com Bootstrap
O layout da aplicação é construído usando Bootstrap, o que garante que a página seja responsiva e visualmente agradável.
O formulário de pesquisa, a tabela de listagem de usuários, e o botão "Novo Usuário" estão centralizados e bem organizados, proporcionando uma experiência de usuário intuitiva.
Os botões de ação "Editar" e "Deletar" possuem estilos visuais claros (como cores diferentes), facilitando a navegação e as operações no sistema.

Fluxo de Funcionamento
Listar e Consultar Usuários:
O usuário acessa a página principal e vê uma lista de usuários registrados no sistema.
Ele pode realizar consultas digitando termos no campo de pesquisa e clicando em "Pesquisar".
A consulta é filtrada e os resultados aparecem em uma tabela.

Criar Novo Usuário:
O usuário clica em "Novo Usuário", preenche o formulário com os detalhes do novo usuário e clica em "Salvar".
O novo registro é inserido no banco de dados e a ação é registrada no log.

Editar Usuário:

O usuário pode clicar em "Editar" para modificar um registro existente.
Após fazer as alterações, o sistema salva as mudanças no banco de dados e registra a ação de edição no log.

Deletar Usuário:
O usuário clica em "Deletar" e confirma a exclusão de um registro.
O registro é removido permanentemente do banco de dados e a ação é registrada no log.

Resumo das Funções

Operações CRUD: Criação, Leitura, Atualização e Exclusão de registros de usuários e produtos.

Consulta: Busca de registros com base em CPF/CNPJ, Nome ou Código do Produto.

Logging: Registro de todas as interações do usuário no sistema, incluindo operações CRUD e consultas, em um arquivo de log diário.

Layout Responsivo: Interface organizada e centralizada, com uso do Bootstrap para um design responsivo e amigável ao usuário.

Prints do funcionamento:

![{1C648A62-746E-4FDB-BA48-B6C8A320FDDC}](https://github.com/user-attachments/assets/6fa49086-ab3d-4ab4-bf03-c498ac750cdf)

![{6BCC345C-910E-4B11-A3F6-AA61B1E8C913}](https://github.com/user-attachments/assets/0c327ca3-eb50-400b-a2fd-d5a46b32f8ef)

![{9EB99385-9218-40BE-8F76-16D2E4EFFF73}](https://github.com/user-attachments/assets/dd352604-c645-40bf-b9bc-ee045cd91c53)

![{C62BCDFE-3894-4C64-B043-4FC507805435}](https://github.com/user-attachments/assets/be34c9fa-e640-4c72-953c-3339619d0451)

Criei um mecanismo que evita duplicidade do cadastro tambem:

![{22772F8A-A832-4F99-B3B8-F47F949C26D4}](https://github.com/user-attachments/assets/99ffc687-3215-480b-8f03-3c7705022361)

Inclui um novo usuario: LUIZ RIBEIRO SILVA
![{9DC13FF8-186B-4A92-A41E-57B0EB3EE446}](https://github.com/user-attachments/assets/202a8f9b-cb8b-4510-b4d4-f8ae86b081da)





