
### Usuários:
- Organizações/projetos pessoais
As organizações são uma funcionalidade do GitHub que permite que grupos de pessoas colaborem de maneira eficaz em projetos de software. As organizações oferecem recursos de gerenciamento de equipes, controle de acesso e permissões, bem como ferramentas de colaboração aprimoradas para projetos de código-fonte aberto ou privados. Esta documentação fornece informações detalhadas sobre como criar, configurar e usar organizações no GitHub, permitindo que equipes e comunidades colaborem de forma mais eficaz em seus projetos.
  
- Comunidade e comentários
A comunidade no GitHub desempenha um papel essencial na evolução e no desenvolvimento de projetos de software. A relação entre a comunidade e os comentários na plataforma é fundamental para aprimorar a qualidade e a eficácia das colaborações. Os comentários são a principal ferramenta de interação, compartilhamento de informações e melhoria de projetos de código-fonte aberto e privados. Por meio de Pull Requests, os membros da comunidade submetem seu trabalho para revisão, permitindo que outros revisem o código, ofereçam sugestões e contribuam para a segurança e a qualidade do código.

Os comentários também desempenham um papel crucial na resolução de problemas, com usuários abrindo issues para relatar bugs e discutir desafios relacionados aos projetos. As discussões são uma parte central da colaboração, sendo usadas para debater ideias, tomar decisões de design e discutir a direção futura dos projetos. Além disso, a comunidade fornece suporte e assistência aos usuários por meio de comentários, respondendo a perguntas e compartilhando conhecimento. A transparência é promovida no GitHub, uma vez que as discussões são públicas, permitindo que todos os membros acessem informações e compreendam o progresso e as decisões no desenvolvimento do software. Essa interação por meio de comentários é um elemento fundamental na cultura de desenvolvimento de código aberto e colaboração em projetos de software globalmente.

- Documentação e Licensas
A documentação e as licenças desempenham papéis importantes na comunidade do GitHub, fornecendo orientação e estrutura para projetos de código aberto e privados.
A documentação é uma parte crucial para qualquer projeto no GitHub. Ela descreve como usar, contribuir e entender o projeto. Muitos projetos mantêm um arquivo README.md no repositório do GitHub, que serve como uma introdução ao projeto e fornece informações básicas, instruções de instalação e exemplos de uso. Além disso, os projetos podem ter guias mais extensos, wikis ou páginas da web externas que detalham aspectos mais complexos do projeto. A documentação ajuda a comunidade a entender o propósito do projeto, como contribuir e como usar o software, facilitando a colaboração eficaz.

As licenças são vitais para a governança dos projetos no GitHub. Elas estabelecem os termos e condições sob os quais o software pode ser usado, modificado e redistribuído. A escolha de uma licença é uma decisão importante para os mantenedores de projetos, pois determina como outros podem usar seu trabalho. Projetos de código aberto geralmente usam licenças de código aberto, como a MIT, a GNU GPL ou a Apache License, que permitem o uso, a modificação e a redistribuição do código, com algumas restrições. As licenças promovem a colaboração aberta e permitem que a comunidade contribua com confiança, sabendo que os termos de uso estão claros.

- Softwares de terceiros como VScode e sua integração
A integração do GitHub com o VSCode e outras ferramentas de desenvolvimento é crucial, simplificando o fluxo de trabalho, oferecendo controle de versão direto, permitindo acesso a recursos do GitHub, assegurando autenticação segura, automatizando tarefas e fornecendo notificações em tempo real. Essa colaboração eficaz economiza tempo, melhora a gestão de projetos e fortalece a segurança, tornando o desenvolvimento mais eficiente e eficaz.

### Segurança: 
- Autenticação dos usuários e organizações 
Usuários do GitHub, incluindo desenvolvedores individuais, colaboradores, profissionais de TI e educadores, utilizam a plataforma para desenvolver, colaborar e aprender. Organizações, como empresas, projetos de código aberto, instituições de ensino e equipes de desenvolvimento, confiam no GitHub para gerenciar e colaborar em projetos de software. O GitHub é uma ferramenta fundamental que apoia uma ampla gama de usuários e organizações em suas atividades de desenvolvimento de software.


- Ataques em repositórios
O GitHub, sendo uma das maiores plataformas de hospedagem de código-fonte, frequentemente se torna alvo de uma variedade de ataques. Os tipos de ataques mais comuns incluem ataques de negação de serviço distribuído (DDoS), onde os servidores do GitHub são sobrecarregados por um grande volume de tráfego malicioso, tornando o serviço inacessível temporariamente. Além disso, ataques de força bruta e tentativas de quebra de senhas também são frequentes, com o objetivo de comprometer contas de usuários. O GitHub tem implementado medidas de segurança avançadas, como proteções contra DDoS e autenticação de dois fatores, para mitigar esses ataques e manter a integridade da plataforma. A segurança cibernética é uma preocupação contínua para o GitHub e outras plataformas semelhantes, dada a importância do desenvolvimento de software e da colaboração online.

### Confiabilidade: 
- Disponibilidade dos repositórios
O GitHub, como uma plataforma de desenvolvimento de software em escala global, depende do MySQL para armazenar e gerenciar uma grande quantidade de dados críticos. O artigo descreve como o GitHub implementou soluções de alta disponibilidade, como a replicação síncrona e a recuperação automática, para garantir a resiliência e a disponibilidade do MySQL em caso de falhas. A abordagem técnica e os detalhes das configurações fornecem uma visão valiosa sobre como o GitHub lida com a infraestrutura crítica para manter sua plataforma de código aberto funcionando de maneira confiável para milhões de desenvolvedores em todo o mundo. É um exemplo de boas práticas de alta disponibilidade em ambientes de desenvolvimento de software de alto desempenho.

- backups 
O GitHub simplificou o processo de backup de repositórios com seu guia "Backing up a repository". Realizar backups regulares é essencial para proteger o trabalho de desenvolvedores contra perdas potenciais devido a falhas de hardware, erros humanos ou ameaças cibernéticas. O processo envolve a clonagem do repositório localmente, uso de serviços como o Git LFS para arquivos grandes e a criação de um arquivo de backup do banco de dados. Este processo, conforme delineado no artigo do GitHub, garante a integridade e a segurança dos dados, permitindo que desenvolvedores protejam seu trabalho valioso de forma eficaz.



# Descrição da arquitetura do GitHub

A arquitetura do GitHub é um sistema complexo e em constante evolução. Aqui estão algumas informações gerais sobre sua arquitetura e decisões de projeto:

### Arquitetura Geral

O GitHub é construído em uma arquitetura de microsserviços, onde diferentes funcionalidades são fornecidas por serviços independentes. Utiliza uma arquitetura orientada a eventos para facilitar a escalabilidade e a manutenção.

### Linguagens de Programação

A base do GitHub é Ruby on Rails, uma estrutura de desenvolvimento web em Ruby, conhecida por sua simplicidade e produtividade. Além do Ruby, o GitHub utiliza outras linguagens, como JavaScript (para o frontend) e várias linguagens para microsserviços específicos.

### Banco de Dados

Inicialmente, o GitHub utilizava MySQL como banco de dados principal. Com o tempo, devido ao crescimento exponencial de dados, começou a adotar tecnologias de banco de dados NoSQL, como o Bigtable do Google Cloud.

### Elasticsearch

O Elasticsearch é usado para recursos de pesquisa, proporcionando uma experiência de pesquisa rápida e eficiente.

### Armazenamento de Dados

O GitHub utiliza o sistema de arquivos distribuído Git para armazenar repositórios de código. Usa Amazon S3 para armazenamento de objetos binários e outros dados.

### Segurança

Incorpora HTTPS em toda a plataforma para garantir a segurança das transações.
Utiliza autenticação de dois fatores (2FA) para proteger as contas dos usuários.

### Microsserviços

A arquitetura de microsserviços permite que diferentes partes da aplicação evoluam independentemente. Cada funcionalidade, como controle de versão, issues, pull requests, etc, é tratada por um microsserviço específico.

### Frontend

Usa React.js para construir interfaces de usuário interativas e responsivas. Adota GraphQL para otimizar as consultas e reduzir a quantidade de dados transferidos.
Integração Contínua/Entrega Contínua (CI/CD):

Adota práticas robustas de CI/CD para automatizar a construção, teste e implantação de software.

### Escalabilidade

A arquitetura foi projetada para escalar horizontalmente, permitindo lidar com um grande volume de tráfego.

### Histórico de Mudanças

O GitHub mantém um registro público de mudanças no repositório GitHub Archive. Muitas decisões de projeto e mudanças específicas podem ser rastreadas nos repositórios públicos do GitHub.

### Desenvolvimento Aberto

O GitHub opera como uma plataforma de desenvolvimento aberto, permitindo que desenvolvedores externos contribuam para projetos de código aberto. É importante notar que essas informações são de natureza geral, e a arquitetura exata e as tecnologias utilizadas podem ter evoluído ao longo do tempo. O GitHub é uma plataforma dinâmica que se adapta para atender às crescentes demandas da comunidade de desenvolvimento.

### Protocolos

O GitHub utiliza três protocolos principais. Esses são SSH, HTTP e Git. O SSH é utilizado quando o usuário está usando operações de “clone”, “push” ou “pull”. Já o HTTP é usado ao navegar no sistema em um navegador. Enquanto o protocolo Git é para quando as operações de “pull” ou “clone” são usadas em um repositório público via URL.

# Descrição das tecnologias

- Git: O GitHub é construído sobre o sistema de controle de versão distribuído Git, desenvolvido por Linus Torvalds. O Git é amplamente utilizado para rastreamento de alterações em código fonte e colaboração entre desenvolvedores.

- REST API: O GitHub expõe uma API RESTful que permite interações programáticas com seus serviços. A API oferece funcionalidades como gerenciamento de repositórios, problemas, pull requests e muito mais. Referência: [GitHub REST API v3][https://docs.github.com/en/rest].

- GraphQL API: Além da REST API, o GitHub também fornece uma API GraphQL que permite aos usuários buscar dados de forma mais flexível e eficiente, adaptando as consultas às suas necessidades específicas. Referência: [GitHub GraphQL API v4][https://docs.github.com/en/graphql].

- Webhooks: O GitHub utiliza webhooks para notificar sistemas externos sobre eventos em repositórios. Isso permite integrações com serviços de CI/CD (Integração Contínua/Entrega Contínua), automações e outras ferramentas. Referência: [GitHub Webhooks][https://docs.github.com/en/developers/webhooks-and-events/webhooks].

- GitHub Actions: Um sistema de automação que permite a criação de fluxos de trabalho personalizados para automação de processos, como CI/CD, teste de código e deploy. Referência: [GitHub Actions][https://docs.github.com/en/actions].

- Git LFS (Large File Storage): Para gerenciar arquivos grandes, o GitHub suporta a extensão Git LFS, que gerencia grandes arquivos binários de forma eficiente. Referência: [Git LFS][https://git-lfs.github.com/].

- OAuth: Para autenticação de usuários e aplicativos de terceiros, o GitHub utiliza o protocolo OAuth. Isso permite que os usuários concedam acesso seguro a seus repositórios sem compartilhar suas credenciais diretamente. Referência: [OAuth][https://docs.github.com/en/developers/apps/building-oauth-apps].

- Actions Runners: Para execução de trabalhos automatizados nos fluxos de trabalho do GitHub Actions, são utilizados agentes chamados Actions Runners. Esses agentes podem ser hospedados em infraestrutura própria ou fornecidos pelo GitHub. Referência: [GitHub Actions Runners][https://docs.github.com/en/actions/hosting-your-own-runners/about-self-hosted-runners].

- Markdown: O GitHub utiliza a linguagem de marcação Markdown para formatação de texto em diversas partes da plataforma, como descrições de repositórios, issues e pull requests. Referência: [Mastering Markdown][https://guides.github.com/features/mastering-markdown/].

- Octicons: Um conjunto de ícones criado pelo GitHub e utilizado em sua interface. Referência: [Octicons][https://octicons.github.com/].


## fontes
- https://github.blog/2023-04-06-building-github-with-ruby-and-rails/
- https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/about-organizations
- https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/about-organizations
- https://docs.github.com/pt/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository
- https://docs.github.com/en/authentication/connecting-to-github-with-ssh
- https://docs.github.com/pt/issues/organizing-your-work-with-project-boards/managing-project-boards/about-project-boards
- https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&ved=2ahUKEwjcoL6gmoOCAxWJq5UCHZkCCn0QFnoECBQQAQ&url=https%3A%2F%2Fdocs.github.com%2Forganizations&usg=AOvVaw3G6SA6DvadLTD17TfFyquZ&opi=89978449
- https://github.blog/changelog/2023-04-28-secret-scanning-now-supports-validation-checks-for-supported-partner-patterns/
- https://github.blog/2022-03-21-validate-all-things-input-validation/
- https://github.blog/2015-03-27-large-scale-ddos-attack-on-github-com/
- https://github.blog/2023-10-11-enforcing-code-reliability-by-requiring-workflows-with-github-repository-rules/
- https://github.blog/2018-06-20-mysql-high-availability-at-github/
- https://github.blog/2016-12-08-orchestrator-github/
- https://github.blog/2018-10-30-oct21-post-incident-analysis/
- https://github.blog/2017-10-12-evolution-of-our-data-centers/
- https://docs.github.com/en/repositories/archiving-a-github-repository/backing-up-a-repository
