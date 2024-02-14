## Projeto Fluxo de Caixa 👋

## Solicitação
Um comerciante necessita de um sistema para gerenciar seu fluxo de caixa diário, registrando todas as 
transações, tanto entradas (créditos) quanto saídas (débitos). Além disso, é essencial que o sistema possa 
fornecer um relatório que apresente o saldo consolidado no final de cada dia.

### Requisitos de negócio
* Desenvolvimento de um serviço que permita o registro e gerenciamento de lançamentos financeiros, 
abrangendo tanto débitos quanto créditos;
* Criação de um serviço que gere relatórios de consolidado diário, apresentando de forma clara e 
organizada o saldo financeiro ao final de cada dia.

### Diagrama de contexto do sistema (Nível 1)
<img src="https://github.com/cleteot/repo-fluxo-caixa/blob/master/Documentacao/01.Diagrama%20de%20contexto%20do%20sistema.png" alt="Diagrama de contexto" with="400px" height="500px">

### Diagrama de container (Nível 2)
<img src="https://github.com/cleteot/repo-fluxo-caixa/blob/master/Documentacao/02.Conteiner.png" alt="Diagrama de container" with="400px" height="500px">

### Diagrama de componente API Application (Nível 3)
<img src="https://github.com/cleteot/repo-fluxo-caixa/blob/master/Documentacao/03.ComponenteAPIApplication.png" alt="Componente API Apllication" with="400px" height="500px">

### Diagrama de componente Mensageria (Nível 3)
<img src="https://github.com/cleteot/repo-fluxo-caixa/blob/master/Documentacao/04.ComponenteMensageria.png" alt="Componente Mensageria" with="400px" height="500px">

## Diagrama de Banco de Dados
<img src="https://github.com/cleteot/repo-fluxo-caixa/blob/master/Documentacao/Diagrama ER de banco de dados Fluxo de Caixa.jpeg" alt="Diagrama de Banco de Dados" with="400px" height="500px">

### Definições Arquiteturais, Padrões de Projeto e Frameworks
**1) Microsserviços**
    Este projeto será desenvolvido em microsserviços, pois este modelo nos orienta a criarmos serviços independentes que por sua vez tem as seguintes vantagens:
- **Descentralização**: Cada microsserviço opera como uma unidade independente e autônoma, geralmente com seu próprio banco de dados.
- **Comunicação**: Os microsserviços se comunicam entre si por meio de interfaces bem definidas, como APIs.
- **Escalabilidade Independente**: Cada serviço pode ser dimensionado separadamente, permitindo melhor escalabilidade.
- **Resiliência**: Se um serviço falha, isso não afeta diretamente outros serviços.
- **Implantação Independente**: Cada serviço pode ser construído, testado e implantado independentemente dos outros.
- Como desvantagem, gerenciar varias partes de sistema e garantir sua consistência.
  
**2) Padrões de Projeto**
  - DDD (Domain-Driven Design)
      - Foca no entendimento profundo do domínio antes da criação de soluções técnicas, o que nos permite primeiro olhar para o negócio e depois como será resolvido técnicamente
  - Repository
      - Fornece uma interface para acessar dados, proporciona um ponto centralizado de leitura e gravação de dados, mantém a lógica de negócios desacopladas.
             
**3) Frameworks**
  - EntityFrameWork (ORM)
      - Permite lidarmos diretamente com o objetos, tem suporte a vários provedores de banco de dados.
  - AutoMapper
      - Como cada camada da aplicação terá seu objeto de entidade, é comum fazermos a correspondência entre este objetos e o AutoMapper agiliza esta tarefa.
  - xUnit
      - Framework para escrever testes unitários, e é possível criar extensões personalizadas para atender requisitos específicos  

## Ferramentas
- Microsoft Visual Studio Community 2022 (64 bits) - Versão 17.8.4 (https://visualstudio.microsoft.com/pt-br/vs/community/)
- Linguagem de programação .Net Core 12
- SDK NET 8 (Fornece suporte a longo prazo) (https://dotnet.microsoft.com/pt-br/download/dotnet/8.0)
- Gerenciador de Banco de Dados MS SQL SERVER 2019
- Gerenciador de Filas de Mensagens RabbitMQ hospedado na AWS
- Docker Desktop para Windows Versão 4.27.1 (https://www.docker.com/)
- WSL 2 (https://apps.microsoft.com/detail/9P9TQF7MRM4R?hl=pt-br&gl=BR)
- Draw.io para criação do Diagrama de Arquitetura
- Lucidchart para criação do Digrama de Banco de Dados
- Git Bash Versão 2.43.0.windows.1 (https://git-scm.com/downloads)
- Terminal do Windows Versão 1.18 (https://apps.microsoft.com/detail/9N0DX20HK701?hl=pt-br&gl=BR)

## Repositórios
  Este projeto contempla 5 reposórios é recomendado que estes esteja seja clonados no mesmo diretórios ficando com a seguinte estrutura.
  Aproveite para acessar cadas um deles e verificar sua documentação

### Pasta Raiz
- [docker](https://github.com/cteotonio-fluxo-caixa/docker)
- [backend-transacoes](https://github.com/cteotonio-fluxo-caixa/backend-transacoes)
- [backend-relatorios](https://github.com/cteotonio-fluxo-caixa/backend-relatorios)
- [backend-usuarios](https://github.com/cteotonio-fluxo-caixa/backend-usuarios)
- [backend-autenticacao-autorizacao](https://github.com/cteotonio-fluxo-caixa/backend-autenticacao-autorizacao)

## ⏭️ Próximos passos

- Criar Microsserviço de Usuários
- Criar Microsserviço de Autenticação Autorização
- Implementar coleta de logs no Splunk
- Implementar versionamento de registros de transações

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->


