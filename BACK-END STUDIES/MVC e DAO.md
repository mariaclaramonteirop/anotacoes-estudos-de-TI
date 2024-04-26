<!--Model -> Nas classes modelo nós definimos os atributos e seus métodos.
- Incluindo métodos acessores, contrutores e funções/métodos caracteristicos da classe.
View -> Parte interativa, lado cliente.
- Telas que o Cliente vai acessar e interagir. Index.html por exemplo
Controller - > Ações que a view vai executar, como adicionar um cliente, atualizar cliente... Ações do CRUD 
Dao -> Ações que a controller vai executar no banco de dados-->

### MVC (Model-View-Controller) e DAO (Data Access Object)

1. **Model (Modelo)**:
   - Representa a estrutura de dados e a lógica de negócios da aplicação.
   - Define os atributos e métodos relacionados a esses dados.
   - Inclui métodos acessores (getters e setters), construtores e outras funções/métodos característicos da classe.
   - Por exemplo, em uma aplicação de gerenciamento de clientes, pode haver uma classe Cliente no modelo, com atributos como nome, email, etc., e métodos para manipular esses dados.

2. **View (Visão)**:
   - É a parte interativa da aplicação, que interage com o usuário.
   - Consiste em interfaces de usuário, como páginas da web, formulários, etc.
   - Por exemplo, a página index.html pode ser uma view que exibe uma lista de clientes em um formato visualmente agradável para o usuário.

3. **Controller (Controlador)**:
   - Responsável por manipular as ações do usuário na interface e atualizar o modelo conforme necessário.
   - Recebe entradas do usuário da view e traduz essas entradas em operações no modelo.
   - Controla o fluxo de dados entre a view e o modelo.
   - Geralmente inclui ações relacionadas ao CRUD (Create, Read, Update, Delete) e outras operações de negócios.
   - Por exemplo, uma ação de adicionar um cliente ou atualizar um cliente seria tratada pela controller.

4. **DAO (Data Access Object)**:
   - Responsável por abstrair o acesso aos dados subjacentes, como um banco de dados.
   - Fornece uma interface para realizar operações de persistência de dados, como salvar, recuperar, atualizar e excluir registros no banco de dados.
   - Ajuda a manter a separação de preocupações, isolando a lógica de acesso a dados do restante da aplicação.
   - Por exemplo, em uma aplicação de gerenciamento de clientes, um DAO para a entidade Cliente seria responsável por executar consultas SQL para manipular os dados do cliente no banco de dados.

Esses componentes trabalham juntos para criar uma aplicação organizada, modular e de fácil manutenção. O MVC separa as preocupações da interface do usuário, da lógica de negócios e do acesso a dados, enquanto o DAO separa a lógica de acesso a dados do restante da aplicação.