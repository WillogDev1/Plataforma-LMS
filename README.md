# Plataforma-LMS

A **Plataforma-LMS** é um sistema de gestão de cursos, trilhas de aprendizado e grupos de alunos focado em olimpíadas escolares, projetado para facilitar a criação, gerenciamento e acompanhamento do progresso educacional. A plataforma oferece uma experiência para alunos e professores, com controle de acesso, pagamento integrado e uma interface intuitiva.

## Regras de Negócio

### Cadastro e Gerenciamento de Professores
- **Cadastro de Professores**: Apenas administradores podem cadastrar novos professores.
- **Gerenciamento de Professores**: Professores podem criar e gerenciar seus próprios cursos, trilhas e grupos de alunos.
- **Vinculação**: Um professor pode ser responsável por vários cursos, trilhas ou grupos.

### Cadastro de Alunos
- **Cadastro Automático**: Alunos podem se cadastrar automaticamente através de um formulário na plataforma ou via integração com o Google.
- **Participação Múltipla**: Alunos podem participar de múltiplas turmas e trilhas simultaneamente.
- **Vinculação**: Cada aluno estará vinculado a um ou mais professores através das turmas.

### Gerenciamento de Cursos e Trilhas
- **Vinculação de Cursos e Trilhas**: Cada curso ou trilha deve ser vinculado a um único professor responsável.
- **Estrutura das Trilhas**: Trilhas podem ser compostas por múltiplos cursos, organizados de forma sequencial ou paralela.
- **Definição de Acesso**: Professores podem definir quais alunos têm acesso a cursos ou trilhas específicas.

### Grupos de Alunos
- **Criação de Grupos**: Professores podem criar grupos específicos de alunos para atividades ou projetos.
- **Participação em Grupos**: Alunos podem pertencer a mais de um grupo, dependendo dos cursos ou trilhas.

### Sistema de Pagamentos
- **Pagamento Necessário**: Alunos devem efetuar pagamento para participar de determinados cursos ou trilhas.
- **Validação de Pagamento**: O sistema valida os pagamentos antes de liberar o acesso aos cursos e conteúdos.

### Acesso Controlado
- **Acesso Restringido**: Apenas professores e alunos cadastrados podem acessar cursos, trilhas e grupos.
- **Permissões de Professores**: Professores têm permissões administrativas sobre os conteúdos que criaram.
- **Permissões de Administrador**: O administrador pode visualizar e gerenciar todos os cursos, trilhas e usuários.

### Plataforma Multidisciplinar
- **Cursos de Diferentes Professores**: Alunos podem participar de cursos oferecidos por diferentes professores na mesma plataforma.
- **Acesso a Cursos de Outros Professores**: Professores não têm acesso aos cursos criados por outros, a menos que o administrador conceda permissões especiais.

## Requisitos do Sistema

### Funcionais

#### Gestão de Usuários
- Cadastro de professores realizado exclusivamente pelo administrador.
- Cadastro automático de alunos com validação de email.
- Painel para gerenciamento de alunos, professores, cursos e trilhas.

#### Criação de Conteúdo
- Professores devem ter uma interface para criar cursos, trilhas e grupos.
- Suporte para upload de materiais didáticos (vídeos, PDFs, links, etc.).
- Professores podem organizar cursos em trilhas de aprendizado.

#### Gestão de Turmas e Grupos
- Permitir que professores adicionem ou removam alunos de grupos e turmas.
- Enviar notificações aos alunos ao serem adicionados a uma turma ou grupo.

#### Sistema de Pagamento
- Integração com gateways de pagamento (ex.: PayPal, Stripe).
- Validação automática de pagamento antes de liberar o acesso aos cursos.

#### Acompanhamento de Progresso
- Alunos podem visualizar seu progresso nos cursos e trilhas.
- Professores podem acessar relatórios de desempenho e progresso dos alunos.

#### Comunicação
- Sistema de mensagens internas para comunicação entre alunos e professores.
- Notificações para alunos sobre atualizações nos cursos ou trilhas.

#### Controle de Acesso
- Diferentes níveis de acesso para administradores, professores e alunos.
- Garantir que apenas usuários autenticados possam acessar os conteúdos da plataforma.

### Não Funcionais

#### Desempenho
- Suportar múltiplos usuários simultaneamente com carregamento eficiente.
- Garantir tempo de resposta inferior a 2 segundos para a maioria das operações.

#### Escalabilidade
- O sistema deve ser escalável para suportar o crescimento do número de usuários, cursos e trilhas.

#### Segurança
- Armazenar senhas de forma segura (ex.: hash com bcrypt).
- Certificado SSL para todas as comunicações.
- Proteção contra ataques comuns (ex.: SQL Injection, Cross-Site Scripting).

#### Usabilidade
- Interface amigável e intuitiva para alunos e professores.
- Compatibilidade com dispositivos móveis e navegadores modernos.

#### Disponibilidade
- O sistema deve ter uma disponibilidade mínima de 99%, garantindo acesso constante aos alunos e professores.

## Fluxo Básico do Sistema

### Administrador
1. Faz login no sistema.
2. Cadastra novos professores.
3. Visualiza relatórios de cursos e alunos.

### Professor
1. Faz login no sistema.
2. Cria cursos, trilhas e grupos.
3. Gerencia os alunos e acompanha o progresso.

### Aluno
1. Se cadastra automaticamente.
2. Efetua pagamento e acessa cursos ou trilhas disponíveis.
3. Participa de grupos e acompanha seu progresso.

## Tecnologias Usadas

A plataforma foi desenvolvida utilizando as seguintes tecnologias e pacotes:

### Tecnologias Principais
- **Laravel**: Framework PHP para o desenvolvimento do backend.
- **Vue.js**: Framework JavaScript para o desenvolvimento da interface do usuário no frontend.
- **PHP**: Linguagem de programação utilizada no backend.
- **MySQL**: Sistema de gerenciamento de banco de dados relacional para armazenar os dados.
- **JavaScript**: Linguagem de programação para interatividade no frontend.

### Pacotes e Ferramentas
- **Jetstream**: Para gerenciamento de autenticação e controle de usuários.
- **Inertia.js**: Para fornecer uma experiência SPA (Single Page Application) sem a necessidade de configurar um frontend separado.
- **Spatie**: Pacote para gerenciamento de permissões e controle de acesso.



## Licença

Este projeto está licenciado sob a licença [Nome da Licença].
