## O que é controle de versões?

Suponha que você esteja alocado em um projeto junto com várias outras pessoas. Cada membro da equipe recebeu tarefas em diferentes módulos do projeto, e todos precisam entregar novas funcionalidades, corrigir bugs, revisar e aplicar melhorias no código, tudo isso em tempo real. Além disso, todos estão fazendo alterações **simultaneamente**.

O controle de versões é uma ferramenta essencial para auxiliar nessa missão. Com ele, todos podem acessar o mesmo projeto e fazer alterações em conjunto, garantindo que as mudanças sejam **organizadas** e **rastreadas**. Além disso, é possível visualizar o histórico de alterações anteriores, permitindo um trabalho colaborativo e seguro.

- **Colaboração**: Todos os membros da equipe podem trabalhar simultaneamente em diferentes módulos do projeto. O sistema de controle de versões permite que essas mudanças sejam integradas de forma organizada, minimizando conflitos.
- **Histórico de mudanças**: Você pode ver o histórico de todas as alterações feitas no projeto, o que facilita a identificação de bugs e o entendimento das razões por trás de certas mudanças.
- **Gerenciamento de conflitos**: Quando duas ou mais pessoas modificam o mesmo arquivo, o sistema de controle de versões ajuda a resolver esses conflitos, integrando as mudanças de maneira segura.
- **Branches**: Em muitos sistemas de controle de versões, como o Git, você pode criar "branches" ou ramificações para trabalhar em novas funcionalidades ou correções sem afetar a versão principal do projeto. Depois, as alterações podem ser integradas de volta à versão principal.

## Versionamento com Git
### O que raios é Git?

Git é uma ferramenta de controle de versões, e se você trabalha com desenvolvimento de software, provavelmente já ouviu falar dela. **Mas, afinal, o que raios é Git e por que todo mundo fala tanto sobre isso?**

Git é como uma máquina do tempo para o seu código. Imagine que você está escrevendo um livro com várias pessoas ao mesmo tempo. Cada um escreve um capítulo, às vezes até ao mesmo tempo, e todos precisam que a versão final faça sentido. Git ajuda a manter tudo organizado, permitindo que você veja quem escreveu o quê, quando e por que fez isso. E se alguém acidentalmente deletar um capítulo inteiro? Sem problemas! Git pode voltar no tempo e recuperar aquela versão perdida.

### E o tal do github?

GitHub é uma **plataforma** baseada na web que usa Git para controle de versões. Pense no GitHub como uma rede social para desenvolvedores, onde eles podem armazenar seus repositórios Git, colaborar com outros desenvolvedores, e compartilhar seus projetos com o mundo.

No github é possível realizar/criar/gerenciar:

1. **Hospedagem de Repositórios**
2. **Colaboração Facilitada**
3. **Controle de Versões na Web**
4. **Integrações e Ferramentas**
5. **Comunidades e Open Source**
6. **Documentação e Wiki**
7. **Issues e Projetos**

### Exemplo de Uso do GitHub

1. **Criar um Repositório**:
    
    - Você começa criando um novo repositório no GitHub, onde você pode armazenar o código do seu projeto.
2. **Clonar o Repositório**:
    
    - Em seu computador, você pode clonar o repositório para começar a trabalhar localmente: `git clone <url-do-repositorio>`.
3. **Fazer Alterações e Commitar**:
    
    - Faça alterações no código, adicione arquivos ao repositório (`git add .`), e crie um commit (`git commit -m "Mensagem do commit"`).
4. **Push para o GitHub**:
    
    - Envie suas alterações de volta para o GitHub com `git push origin main` (ou outra branch).
5. **Abrir um Pull Request**:
    
    - Se você estiver colaborando em um projeto, pode abrir um pull request para que suas mudanças sejam revisadas e potencialmente mescladas ao branch principal.
6. **Revisar e Mesclar**:
    
    - Outros desenvolvedores podem revisar seu pull request, deixar comentários, solicitar mudanças, e eventualmente mesclar suas alterações.

### Ferramentas semelhantes ao Github
Existem várias plataformas semelhantes ao GitHub que oferecem funcionalidades de controle de versões, colaboração e hospedagem de repositórios. Aqui estão algumas das principais alternativas:

### 1. **GitLab**

- **Descrição**: GitLab é uma plataforma de DevOps completa que oferece controle de versões, CI/CD (Integração Contínua/Entrega Contínua), e ferramentas de gerenciamento de projetos. Diferentemente do GitHub, GitLab é conhecido por sua versão auto-hospedada, o que significa que você pode instalar o GitLab em seus próprios servidores.
- **Diferenciais**: Oferece uma integração mais profunda com ferramentas DevOps, incluindo pipelines de CI/CD. Possui recursos avançados para automação de deploys e gestão de segurança de código.

### 2. **Bitbucket**

- **Descrição**: Bitbucket é uma plataforma de hospedagem de repositórios Git, mantida pela Atlassian (a mesma empresa responsável pelo Jira e Confluence). É integrado de forma nativa com outras ferramentas Atlassian, facilitando a gestão de projetos em ambientes corporativos.
- **Diferenciais**: Suporte ao sistema de controle de versões Mercurial (embora o suporte ao Mercurial tenha sido descontinuado em 2020). Integração nativa com Jira, uma ferramenta popular de gestão de projetos.

### 3. **SourceForge**

- **Descrição**: SourceForge é uma das mais antigas plataformas de hospedagem de projetos de código aberto. Embora tenha perdido popularidade nos últimos anos, ainda é uma escolha para muitos projetos de código aberto.
- **Diferenciais**: Oferece uma vasta biblioteca de projetos de código aberto, fóruns, e recursos para colaboração. Também suporta múltiplos sistemas de controle de versões, como Git, Subversion, e Mercurial.

### 4. **Azure DevOps (antigo Visual Studio Team Services, VSTS)**

- **Descrição**: Azure DevOps, da Microsoft, é uma plataforma de DevOps que inclui hospedagem de repositórios Git, integração contínua, e ferramentas de gerenciamento de projetos. É parte do ecossistema Azure, mas pode ser usada de forma independente.
- **Diferenciais**: Integração com o Azure, facilitando o deploy de aplicativos diretamente na nuvem. Ferramentas robustas para planejamento de projetos e rastreamento de tarefas.

### 5. **Gitea**

- **Descrição**: Gitea é uma plataforma de hospedagem de repositórios Git de código aberto, leve e fácil de configurar. É uma alternativa auto-hospedada para quem busca uma solução simples e eficiente.
- **Diferenciais**: Extremamente leve e rápida de configurar. Ideal para quem quer controlar completamente sua infraestrutura e prefere uma solução minimalista.

### 6. **Phabricator**

- **Descrição**: Phabricator é uma plataforma de desenvolvimento de software que inclui controle de versões, revisão de código, e ferramentas de gerenciamento de tarefas. É desenvolvido e mantido pela Phacility.
- **Diferenciais**: Oferece um conjunto de ferramentas mais voltado para o desenvolvimento colaborativo, com forte ênfase na revisão de código e discussões técnicas.

### 7. **Launchpad**

- **Descrição**: Launchpad é uma plataforma de desenvolvimento de software mantida pela Canonical, a empresa por trás do Ubuntu. É usada principalmente para projetos de código aberto.
- **Diferenciais**: Suporte a bugs, tradução de software e construção de pacotes de software. Muito usada pela comunidade Ubuntu para desenvolvimento e manutenção de pacotes.