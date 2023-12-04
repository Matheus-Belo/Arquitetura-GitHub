
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

### Git
O GitHub é construído sobre o sistema de controle de versão distribuído Git, desenvolvido por Linus Torvalds. O Git é amplamente utilizado para rastreamento de alterações em código fonte e colaboração entre desenvolvedores.

### REST API 
O GitHub expõe uma API RESTful que permite interações programáticas com seus serviços. A API oferece funcionalidades como gerenciamento de repositórios, problemas, pull requests e muito mais. Referência: [GitHub REST API v3][https://docs.github.com/en/rest].

### GraphQL API
Além da REST API, o GitHub também fornece uma API GraphQL que permite aos usuários buscar dados de forma mais flexível e eficiente, adaptando as consultas às suas necessidades específicas.

Aqui estão alguns exemplos práticos de como você pode usar a API GraphQL do GitHub:

- **Obtendo Informações de um Repositório:**
```
query {
  repository(owner: "owner", name: "repo") {
    name
    description
    stargazerCount
    forkCount
  }
}
```

- **Listando Issues em um Repositório:**
```
query {
  repository(owner: "owner", name: "repo") {
    issues(states: OPEN) {
      nodes {
        title
        body
      }
    }
  }
}
```

- **Criando uma Issue:**
```
mutation {
  createIssue(input: { repositoryId: "repoID", title: "Nova Issue", body: "Descrição da nova issue" }) {
    issue {
      title
      body
    }
  }
}
```  

- **Obtendo a Lista de Branches:**
```
query {
  repository(owner: "owner", name: "repo") {
    refs(refPrefix: "refs/heads/", first: 10) {
      nodes {
        name
      }
    }
  }
}
```

- **Obtendo a Lista de Commits:**
```
query {
  repository(owner: "owner", name: "repo") {
    defaultBranchRef {
      target {
        ... on Commit {
          history(first: 10) {
            nodes {
              message
              author {
                name
              }
            }
          }
        }
      }
    }
  }
}

```

Referência: [GitHub GraphQL API v4][https://docs.github.com/en/graphql].

### Webhooks 
Os webhooks são mecanismos de comunicação entre sistemas, permitindo que um aplicativo ou serviço seja notificado automaticamente quando eventos específicos ocorrem em outro sistema. Em termos simples, um webhook é uma forma de automatizar a comunicação entre diferentes serviços na web.

No contexto do GitHub, os webhooks são usados para que eventos dentro de um repositório (como push de código, criação de issues, pull requests, etc.) acionem a execução de ações em serviços externos. Em vez de verificar manualmente por alterações, o GitHub envia automaticamente uma solicitação HTTP para um URL específico (o endpoint do webhook) sempre que um evento ocorre.
Aqui estão os passos básicos de como os webhooks funcionam:

- Configuração:
	O administrador do repositório configura um webhook no GitHub, fornecendo a URL do serviço externo que deve ser notificado.

- Registro de Eventos:
	O administrador do repositório escolhe quais eventos específicos devem acionar o webhook (por exemplo, push de código, criação de issues, etc.).

- Evento Ocorre:
	Quando o evento escolhido ocorre (por exemplo, alguém faz push de código para o repositório), o GitHub envia uma solicitação HTTP POST para a URL do webhook configurada.

- Processamento Externo:
	O serviço externo recebe a solicitação do webhook e executa ações específicas com base nos dados do evento. Isso pode incluir a execução de testes automáticos, integração contínua, notificações, entre outras coisas.

No GitHub, os webhooks são usados para uma variedade de propósitos, incluindo:

- Integração Contínua (CI/CD): Notificar serviços de integração contínua quando novos commits são enviados para um repositório.

- Automação de Fluxo de Trabalho: Acionar scripts ou processos automatizados em resposta a eventos específicos, como a criação de pull requests.

- Notificações: Integrar serviços de notificação para alertar equipes sobre atividades importantes em um repositório.

Para configurar um webhook no GitHub, você normalmente precisa fornecer a URL do endpoint do webhook, escolher os eventos que deseja monitorar e configurar opções adicionais, como segredos para autenticação.

Referência: [GitHub Webhooks][https://docs.github.com/en/developers/webhooks-and-events/webhooks].

### GitHub Actions 
O GitHub Actions é uma ferramenta poderosa de automação integrada diretamente ao GitHub, permitindo que você automatize fluxos de trabalho (workflows) para construir, testar, empacotar e implantar projetos diretamente do seu repositório GitHub.

Aqui está um exemplo prático de como você pode usar o GitHub Actions para executar testes automatizados em um projeto Node.js:

1. **Crie um Arquivo de Configuração para o Workflow:**
   Crie um arquivo chamado `.github/workflows/test.yml` no seu repositório. Este arquivo conterá a configuração do seu workflow.
name: Testes Node.js
```yaml
on: [push, pull_request]

jobs:
  test:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout do Código
      uses: actions/checkout@v2

    - name: Configurar Node.js
      uses: actions/setup-node@v3
      with:
        node-version: 14

    - name: Instalar Dependências
      run: npm install

    - name: Executar Testes
      run: npm test
```
2. **Commit e Push:**
   Faça um commit e push do arquivo de configuração do workflow para o seu repositório.
```bash
git add .github/workflows/test.yml
git commit -m "Adicionar workflow de testes"
git push
```

3. **Veja o Workflow em Ação:**
Vá até a seção "Actions" no seu repositório no GitHub. Você verá o status do workflow de testes em execução. O GitHub Actions executará automaticamente o workflow sempre que houver um push ou pull request, proporcionando automação contínua.

Referência: [GitHub Actions][https://docs.github.com/en/actions].

### Git LFS (Large File Storage)
O Git Large File Storage (LFS) é uma extensão do Git que lida especificamente com grandes arquivos binários, ajudando a melhorar o desempenho do Git ao lidar com esses tipos de arquivos. Ele substitui automaticamente grandes arquivos binários no seu repositório Git por referências pequenas, mantendo os arquivos reais em um armazenamento externo.

Aqui está um exemplo prático do uso do Git LFS:
###### Configuração Inicial

1. **Instalar o Git LFS:** Certifique-se de ter o Git LFS instalado no seu sistema. Você pode baixá-lo e instalá-lo a partir do site oficial ou usar um gerenciador de pacotes.

2. **Iniciar um Novo Repositório:** Crie um novo repositório Git ou use um existente.
`git init`

3. **Configurar o Git LFS:** Ative o Git LFS no repositório.
`git lfs install`

###### Adicionar Arquivos Binários
**Rastrear Tipos de Arquivos com o Git LFS:** Digamos que você tenha um arquivo binário grande, como um arquivo de imagem, que você deseja rastrear com o Git LFS. Use o seguinte comando para rastrear arquivos com a extensão .png:
`git lfs track "*.png"`
Isso cria ou atualiza o arquivo `.gitattributes`, indicando ao Git LFS para gerenciar os arquivos com a extensão .png .

-**Adicionar e Comitar Arquivos:**
Adicione e confirme os arquivos ao repositório.
`git add .`
`git commit -m "Adicionar arquivos PNG usando Git LFS"`
Ao commitar, o Git LFS substituirá automaticamente os arquivos binários pelo ponteiro correspondente.

- **Push para o Repositório Remoto:**
Faça o push dos seus commits para o repositório remoto.
`git push origin master`
###### Clone e Pull em Outros Locais

- **Clone do Repositório em Outro Local:** Em outro local, clone o repositório.
  `git clone https://github.com/seu-usuario/seu-repositorio.git`
  
- **Pull dos Arquivos com o Git LFS:** Quando você clona ou faz pull em um repositório com arquivos gerenciados pelo Git LFS, você precisa garantir que tenha o Git LFS instalado e executar o comando `git lfs pull` para baixar os arquivos reais.
`git lfs pull`


Referência: [Git LFS][https://git-lfs.github.com/].

### OAuth
OAuth (Open Authorization) é um protocolo de autorização amplamente utilizado na web para permitir que aplicativos e serviços obtenham acesso autorizado a recursos em nome de um usuário, sem a necessidade de compartilhar suas credenciais de login. O OAuth é comumente usado em cenários nos quais um aplicativo precisa acessar dados protegidos ou realizar ações em nome do usuário em serviços web.

Aqui está uma explicação geral de como o OAuth funciona:

- **Solicitação de Autorização:** O aplicativo cliente (que deseja acessar recursos protegidos) redireciona o usuário para o provedor de serviços (como o GitHub) para autenticação.
- **Autenticação do Usuário:**  O usuário fornece suas credenciais ao provedor de serviços e autentica-se.
- **Concessão de Autorização:** Após a autenticação bem-sucedida, o provedor de serviços pede ao usuário para conceder permissão ao aplicativo cliente.
- **Obtenção do Token de Acesso:** Uma vez concedida a permissão, o provedor de serviços emite um token de acesso para o aplicativo cliente.
- **Acesso aos Recursos Protegidos:** O aplicativo cliente usa o token de acesso para fazer solicitações aos recursos protegidos em nome do usuário.

Agora, um exemplo prático do uso do OAuth no GitHub:
- **Registro do Aplicativo no GitHub:**  Para usar o OAuth no GitHub, você primeiro precisa registrar seu aplicativo no GitHub. Isso envolve fornecer informações como o nome do aplicativo, uma descrição e a URL de redirecionamento.
- **Obtenção das Credenciais do Cliente:** Após o registro, você recebe um Client ID e um Client Secret. Essas são suas credenciais de cliente.
- **Redirecionamento do Usuário para a Página de Autorização do GitHub:** Quando um usuário deseja usar seu aplicativo, você redireciona o usuário para a página de autorização do GitHub, incluindo seu Client ID e uma URL de redirecionamento.
 `https://github.com/login/oauth/authorize client_id=SEU_CLIENT_ID&redirect_uri=SUA_URL_DE_REDIR`
- **Autorização do Usuário:** O usuário faz login no GitHub (se ainda não estiver logado) e concede permissões ao seu aplicativo.
- **GitHub Redireciona de Volta com o Código de Autorização:** Após a autorização, o GitHub redireciona o usuário de volta para a URL de redirecionamento do seu aplicativo, incluindo um código de autorização.
- **Obtenção do Token de Acesso:** Seu servidor de back-end troca o código de autorização por um token de acesso, fazendo uma solicitação para a URL do token do GitHub.
`POST https://github.com/login/oauth/access_token`   
- **Acesso aos Recursos Protegidos:** Com o token de acesso, seu aplicativo pode fazer solicitações à API do GitHub em nome do usuário autenticado.

Este é um fluxo básico do OAuth no contexto do GitHub. O uso do OAuth é uma prática comum para integrar aplicativos de terceiros com serviços web, como o GitHub, de maneira segura e sem a necessidade de compartilhar senhas.

Referência: [OAuth][https://docs.github.com/en/developers/apps/building-oauth-apps].

### Actions Runners 
GitHub Actions Runners são máquinas virtuais ou físicas configuradas para executar trabalhos (jobs) em GitHub Actions. Os runners permitem que você execute seus fluxos de trabalho (workflows) em ambientes personalizados, proporcionando flexibilidade para realizar tarefas específicas do seu projeto. Os runners podem ser hospedados pelo GitHub (runners hospedados) ou por você mesmo (runners auto-hospedados).

- **GitHub Actions Runner Hospedado:** O GitHub fornece runners hospedados em execução em ambientes virtuais gerenciados pelo GitHub. Eles são adequados para a maioria dos casos de uso.
- **GitHub Actions Runner Auto-hospedado:** Você pode configurar e hospedar seus próprios runners em seus próprios ambientes, como máquinas físicas, VMs ou contêineres, permitindo maior personalização e controle.

**Exemplo prático**: Um exemplo prático usando GitHub Actions com um runner hospedado para realizar uma simples tarefa de CI/CD (Integração Contínua e Implantação Contínua):

- **Criar um Arquivo de Configuração do Workflow:** Crie um arquivo chamado `.github/workflows/main.yml` no seu repositório
```yaml
name: CI/CD Pipeline

on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout do Código
      uses: actions/checkout@v2

    - name: Configurar Node.js
      uses: actions/setup-node@v3
      with:
        node-version: 14

    - name: Instalar Dependências
      run: npm install

    - name: Executar Testes
      run: npm test

    - name: Fazer Deploy (Simulado)
      run: echo "Deploying to production..."

```
Este exemplo cria um workflow que é acionado em cada push para a branch `main`. Ele usa um runner hospedado com Ubuntu, configura o Node.js, instala as dependências do projeto, executa os testes e, em seguida, realiza uma simulação de implantação.

**Commit e Push:** Um commit e push do arquivo de configuração do workflow para o seu repositório.
```bash
git add .github/workflows/main.yml
git commit -m "Adicionar workflow de CI/CD"
git push
```

- **Veja o Workflow em Ação:** Vá até a seção "Actions" no seu repositório no GitHub. Você verá o status do workflow de CI/CD em execução. O GitHub Actions executará automaticamente o workflow sempre que houver um push na branch `main`.

Referência: [GitHub Actions Runners][https://docs.github.com/en/actions/hosting-your-own-runners/about-self-hosted-runners].

### Markdown
O Markdown é uma linguagem de marcação leve que é amplamente utilizada para formatação de texto na web. No contexto do GitHub, o Markdown é usado para formatar READMEs de repositórios, issues, pull requests, e outros documentos. Ele fornece uma maneira simples e legível de criar documentos com formatação básica, como títulos, listas, links, imagens e mais.

Aqui está um exemplo prático de como usar Markdown no GitHub:

- **Criar um Arquivo README.md:** Em um repositório do GitHub, adicione um arquivo chamado `README.md`. Este arquivo será exibido na página inicial do seu repositório.
  
- **Adicionar Títulos:** Use `#` para criar títulos. Quanto mais `#` você usar, menor será o título.
```
# Meu Projeto

## Introdução

Bem-vindo ao meu projeto!
```

- **Criar Listas:** Use `*` ou `-` para criar listas não ordenadas e números para listas ordenadas.
```
## Recursos

- Funcionalidade A
- Funcionalidade B
- Funcionalidade C

## Tarefas Pendentes

1. Implementar Funcionalidade A
2. Testar Funcionalidade B
3. Corrigir Bug em C
```

- **Adicionar Links:** Use `[Texto do Link](URL)` para adicionar links.
```
## Saiba Mais

Para obter mais informações, visite [a página oficial](https://exemplo.com).
```

Referência: [Mastering Markdown][https://guides.github.com/features/mastering-markdown/].

### Octicons
Os Octicons são um conjunto de ícones vetoriais criados pela GitHub. Eles são usados na interface do usuário do GitHub para fornecer ícones consistentes e amigáveis em toda a plataforma. Os ícones são projetados para serem usados em diversas situações, desde navegação até ações específicas do usuário.

Os Octicons podem ser usados não apenas na interface do usuário do GitHub, mas também em projetos externos. GitHub disponibiliza os Octicons como uma fonte, o que facilita sua inclusão em projetos web.

Aqui está um exemplo prático do uso de Octicons em um arquivo Markdown no GitHub:

```
## Exemplo com Octicons

- Ícone de problema (issue):
  - :bug: `:bug:` - Resolveu um problema!

- Ícone de solicitação de pull (pull request):
  - :pull_request: `:pull_request:` - Solicitou um pull request!

- Ícone de estrela (star):
  - :star: `:star:` - Estrelou este projeto!

- Ícone de olho (watch):
  - :eyes: `:eyes:` - Está observando este repositório!

- Ícone de forquilha (fork):
  - :fork_and_knife: `:fork_and_knife:` - Fez um fork deste projeto!

- Ícone de balão de diálogo (comment):
  - :speech_balloon: `:speech_balloon:` - Comentou em uma issue!

- Ícone de coração (heart):
  - :heart: `:heart:` - Ama o GitHub!
```

Para usar esses ícones em seus próprios documentos Markdown no GitHub, basta copiar e colar os códigos correspondentes. Os códigos entre colons (`:código:`) são substituídos pelos ícones correspondentes quando renderizados no GitHub.

Referência: [Octicons][https://octicons.github.com/].


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
