# Snyk + SonarQube
## Ferramentas de Segurança e Qualidade no DevSecOps

>**Trabalho da disciplina de Engenharia de Software**  **Ferramentas:** Snyk e SonarQube | **Tema:** DevSecOps | **Turma:** Sexta-feira


## Sumário

- [Introdução](#introdução)
- [Sobre as Ferramentas](#sobre-as-ferramentas)
- [Comparativo: Snyk vs SonarQube](#comparativo-snyk-vs-sonarqube)
- [Instalação e Configuração](#instalação-e-configuração)
- [Exemplo de Demonstração Funcional](#exemplo-de-demonstração-funcional)
- [Dificuldades Encontradas](#dificuldades-encontradas)
- [Conclusão](#conclusão)
- [Referências](#referências)


## Introdução

**DevSecOps** é a prática de integrar a segurança ao ciclo de vida do desenvolvimento de software, desde a concepção até a produção. O conceito de **"Shift Left"** (deslocar para a esquerda) propõe que a segurança seja considerada nas fases iniciais do desenvolvimento, em vez de ser uma etapa final e isolada.

Neste trabalho, exploramos duas ferramentas essenciais para o ecossistema DevSecOps: **Snyk** (focado em segurança de dependências e containers) e **SonarQube** (focado em qualidade e análise estática de código).

> **Objetivo:** Demonstrar como essas ferramentas se complementam para garantir que o código seja não apenas funcional, mas também seguro, limpo e de fácil manutenção.


## Sobre as Ferramentas

### 🔹 SonarQube

O **SonarQube** é uma plataforma open source criada em 2006 por Olivier Gaudin, Freddy Mallet e Simon Brandhof. Inicialmente chamado apenas de "Sonar", foi desenvolvido para preencher a lacuna de ferramentas que analisassem automaticamente a qualidade do código durante o desenvolvimento.

Mantido atualmente pela empresa **SonarSource**, o SonarQube realiza análise estática de código, identificando:

* **Bugs:** problemas que podem causar comportamento incorreto do software.
* **Vulnerabilidades:** falhas de segurança no código-fonte.
* **Code Smells:** trechos de código que dificultam a manutenção e compreensão.
* **Métricas:** cobertura de testes, duplicação de código e dívida técnica.

> **Curiosidade:** O SonarQube suporta mais de **30 linguagens** de programação, incluindo Java, Python, JavaScript, C#, C++, Go e TypeScript.

### 🔹 Snyk

O **Snyk** é uma plataforma de segurança nativa em nuvem, fundada em 2015 por Guy Podjarny, Assaf Hefetz e Danny Grander. A ferramenta foi criada com a filosofia **"Developer First"** (primeiro o desenvolvedor), tornando a segurança acessível e acionável para quem escreve o código.

O Snyk atua em múltiplas frentes:

* **Snyk Open Source (SCA):** Escaneia dependências e bibliotecas de terceiros em busca de vulnerabilidades conhecidas (CVEs).
* **Snyk Code (SAST):** Analisa o código-fonte em busca de falhas de segurança usando IA (DeepCode AI).
* **Snyk Container:** Verifica imagens Docker em busca de vulnerabilidades em pacotes do sistema operacional.
* **Snyk IaC:** Avalia arquivos de infraestrutura como código (Terraform, Kubernetes, CloudFormation).

> **Diferencial:** O Snyk é conhecido por gerar **Pull Requests automáticos** com as correções sugeridas para vulnerabilidades em dependências.



## Comparativo: Snyk vs SonarQube

Embora ambas sejam ferramentas de segurança, elas atuam em camadas diferentes e são **complementares**. Enquanto o SonarQube cuida da **qualidade interna** do código, o Snyk protege a **cadeia de suprimentos** (dependências externas e containers).

| Critério | Snyk | SonarQube |
| :--- | :--- | :--- |
| **Foco principal** | Segurança de aplicações (AppSec) | Qualidade de código + SAST |
| **Especialidade** | SCA (dependências), containers e IaC | Análise estática (lógica, bugs, manutenibilidade) |
| **Abordagem** | "Corrija esta vulnerabilidade específica" | "Melhore a estrutura e segurança do seu código" |
| **Remediação** | Pull Requests automáticos | Sugestões de refatoração |
| **Modelo** | SaaS (nuvem) ou Broker | Self-Hosted ou SaaS (SonarCloud) |
| **Plano gratuito** | Sim (com limitações) | Community Edition (completa) |

### Por que usar ambos?

Em um pipeline de DevSecOps maduro, as ferramentas se complementam:

* **SonarQube** -> Primeira linha de defesa. Evita que o desenvolvedor cometa erros de lógica, segurança ou boas práticas no código que ele mesmo escreve.
* **Snyk** -> Especialista em cadeia de suprimentos. Garante que as bibliotecas externas utilizadas não tragam vulnerabilidades conhecidas para o projeto.

> **Cenário ideal:** **SNYK** + **SONARQUBE** trabalhando juntos no pipeline CI/CD.

---

## Instalação e Configuração

### Instalação do SonarQube

Para esta demonstração, utilizamos a versão **SonarCloud** (SaaS), dispensando a instalação de um servidor local. O SonarCloud é gratuito para repositórios públicos e se integra nativamente ao GitHub.

**Passos realizados:**

1. Acessar [sonarcloud.io](https://sonarcloud.io) e fazer login com a conta GitHub.
2. Clicar em **"Analyze new project"** e selecionar o repositório desejado.
3. Configurar o **Quality Gate** (critérios mínimos de qualidade).
4. Obter o **SONAR_TOKEN** para integração com o pipeline.

## 💻 Exemplo de Demonstração Funcional

Para a demonstração, foi analisado um projeto real: um site de denúncia sobre infraestrutura em Palmas, desenvolvido como projeto final de um curso técnico.

O fluxo da demonstração foi estruturado nos seguintes passos:
1. Criar o projeto local no SonarQube.
2. Rodar o scanner na pasta do projeto.
3. Visualizar o relatório gerado no dashboard.

![Demonstração Funcional](demonstracao.png)


##  Dificuldades Encontradas

### 1. Configuração do GitHub App *(A mais trabalhosa)*
* **Erro:** `Missing permissions (pull_requests: null, checks: null)`
* **Solução:** Ajustar as permissões para **Read & Write** nas configurações do GitHub App.
* **Erro:** `redirect_uri not associated`
* **Solução:** Adicionar `http://localhost:9000/oauth2/callback/github` no campo **Callback URL**.

### 2. Comunicação Docker com Windows *(muito técnica)*
* **Erro:** `Failed to query server version` (o sistema não encontrava o SonarQube).
* **Solução:** Descobrir que o Docker no WSL2 possui um IP próprio (`172.23.99.192`) e utilizá-lo no comando no lugar do `localhost`.

### 3. Erros de Sintaxe no Comando
* **Erro:** `Unrecognized option: .projectKey`
* **Solução:** Corrigir a digitação do comando enviado ao terminal (faltava o prefixo `-D`).

### 4. Interface pouco intuitiva do SonarQube
* **Dificuldade:** Encontrar onde importar o repositório ou testar a configuração inicial.
* **Solução:** Explorar os menus internos seguindo o caminho: `Administration` ➔ `DevOps Platform Integrations` ➔ `GitHub`.

## Conclusão

O trabalho demonstrou que o **Snyk** e o **SonarQube** são ferramentas complementares e essenciais em um ambiente DevSecOps maduro:

* **SonarQube:** É a ferramenta ideal para garantir a **qualidade interna** do código, detectando bugs, vulnerabilidades e *code smells* diretamente no código-fonte.
* **Snyk:** É especialista na **segurança da cadeia de suprimentos**, protegendo o projeto contra vulnerabilidades em dependências, containers e infraestrutura como código (IaC).

Recomendamos o uso de ambas as ferramentas em projetos de médio e grande porte, especialmente aqueles desenvolvidos em equipe, onde garantir a segurança e a evolução sustentável do software é essencial. O investimento em configuração e aprendizado é amplamente compensado pela **redução de riscos** e pela **automação** da detecção de problemas.

>  **Mensagem final:** No DevSecOps, a segurança não é uma etapa final — é um processo contínuo que começa na primeira linha de código.


## Referências

* [SonarQube — Site oficial](https://www.sonarsource.com/products/sonarqube/)
* [Documentação oficial do SonarQube](https://docs.sonarqube.org/latest/)
* [Snyk — Site oficial](https://snyk.io/)
* [Documentação oficial do Snyk](https://docs.snyk.io/)
* [Snyk: Developer-first security](https://about.snyk.io/)
* [GitHub Actions — Documentação](https://github.com/features/actions)
* [What is DevSecOps? — DevOps.com](https://devops.com/what-is-devsecops/)
* [Material gerado durante a etapa de instalação e testes práticos](https://docs.google.com/document/d/19fd-NdfAgCPUOqKqsN2uQ8wOY7gzLmBPpQFvUQEKFak/edit?usp=sharing)