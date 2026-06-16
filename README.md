olaaaaaaaaaaaaaaaaaaa<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>README - Snyk e SonarQube no DevSecOps</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.8;
            color: #2d3748;
            background: #f7fafc;
            padding: 40px 20px;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            background: #ffffff;
            padding: 50px 60px;
            border-radius: 16px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.08);
        }

        h1 {
            font-size: 2.4rem;
            color: #1a202c;
            border-bottom: 4px solid #4299e1;
            padding-bottom: 16px;
            margin-bottom: 8px;
        }

        .subtitle {
            font-size: 1.1rem;
            color: #4a5568;
            margin-bottom: 32px;
            padding: 12px 20px;
            background: #ebf8ff;
            border-left: 4px solid #4299e1;
            border-radius: 4px;
        }

        h2 {
            font-size: 1.8rem;
            color: #2b6cb0;
            margin-top: 40px;
            margin-bottom: 16px;
            padding-bottom: 8px;
            border-bottom: 2px solid #e2e8f0;
        }

        h3 {
            font-size: 1.3rem;
            color: #2d3748;
            margin-top: 28px;
            margin-bottom: 12px;
        }

        h4 {
            font-size: 1.1rem;
            color: #4a5568;
            margin-top: 20px;
            margin-bottom: 8px;
        }

        p {
            margin-bottom: 16px;
            text-align: justify;
        }

        ul, ol {
            margin: 12px 0 20px 28px;
        }

        li {
            margin-bottom: 8px;
        }

        .highlight-box {
            background: #edf2f7;
            border-left: 4px solid #4299e1;
            padding: 16px 24px;
            margin: 20px 0;
            border-radius: 4px;
        }

        .code-block {
            background: #2d3748;
            color: #e2e8f0;
            padding: 16px 20px;
            border-radius: 8px;
            font-family: 'Courier New', monospace;
            font-size: 0.9rem;
            overflow-x: auto;
            margin: 16px 0;
            white-space: pre-wrap;
            word-break: break-all;
        }

        .code-block code {
            color: #fbd38d;
        }

        .inline-code {
            background: #edf2f7;
            padding: 2px 8px;
            border-radius: 4px;
            font-family: 'Courier New', monospace;
            font-size: 0.9rem;
            color: #2b6cb0;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            font-size: 0.95rem;
        }

        table th {
            background: #2b6cb0;
            color: white;
            padding: 12px 16px;
            text-align: left;
        }

        table td {
            padding: 12px 16px;
            border-bottom: 1px solid #e2e8f0;
        }

        table tr:hover {
            background: #f7fafc;
        }

        .tag {
            display: inline-block;
            padding: 2px 12px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
        }

        .tag-danger {
            background: #fed7d7;
            color: #9b2c2c;
        }

        .tag-warning {
            background: #feebc8;
            color: #9c4221;
        }

        .tag-info {
            background: #bee3f8;
            color: #2a4365;
        }

        .tag-success {
            background: #c6f6d5;
            color: #276749;
        }

        .badge {
            display: inline-block;
            padding: 4px 12px;
            border-radius: 4px;
            font-size: 0.75rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .badge-snyk {
            background: #4a4a4a;
            color: #ffffff;
        }

        .badge-sonar {
            background: #4e9cd4;
            color: #ffffff;
        }

        .comparison-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 24px;
            margin: 20px 0;
        }

        .comparison-card {
            background: #f7fafc;
            border-radius: 8px;
            padding: 20px 24px;
            border: 1px solid #e2e8f0;
        }

        .comparison-card h4 {
            margin-top: 0;
            color: #2b6cb0;
        }

        .comparison-card ul {
            margin-left: 16px;
        }

        hr {
            border: 0;
            border-top: 2px solid #e2e8f0;
            margin: 40px 0;
        }

        .footer {
            margin-top: 40px;
            padding-top: 24px;
            border-top: 2px solid #e2e8f0;
            font-size: 0.9rem;
            color: #718096;
            text-align: center;
        }

        @media (max-width: 768px) {
            .container {
                padding: 24px 20px;
            }

            h1 {
                font-size: 1.8rem;
            }

            .comparison-grid {
                grid-template-columns: 1fr;
            }

            table {
                font-size: 0.8rem;
            }

            table th,
            table td {
                padding: 8px 10px;
            }
        }
    </style>
</head>
<body>

    <div class="container">

        <!-- TÍTULO PRINCIPAL -->
        <h1>🔒 Snyk + SonarQube</h1>
        <h1 style="font-size: 1.6rem; border-bottom: none; padding-bottom: 0; margin-top: -8px; color: #4a5568;">
            Ferramentas de Segurança e Qualidade no DevSecOps
        </h1>

        <div class="subtitle">
            <strong>Trabalho da disciplina de Engenharia de Software — Curso de Ciência da Computação</strong><br>
            Tema da aula: <strong>DevSecOps</strong> | Ferramentas escolhidas: <strong>Snyk</strong> e <strong>SonarQube</strong>
        </div>

        <!-- SUMÁRIO -->
        <h2>📑 Sumário</h2>
        <ul>
            <li><a href="#introducao">Introdução</a></li>
            <li><a href="#sobre">Sobre as Ferramentas</a></li>
            <li><a href="#comparacao">Comparativo: Snyk vs SonarQube</a></li>
            <li><a href="#instalacao">Instalação e Configuração</a></li>
            <li><a href="#demonstracao">Exemplo de Demonstração Funcional</a></li>
            <li><a href="#resultados">Resultados da Análise</a></li>
            <li><a href="#dificuldades">Dificuldades Encontradas</a></li>
            <li><a href="#conclusao">Conclusão</a></li>
            <li><a href="#referencias">Referências</a></li>
        </ul>

        <hr>

        <!-- 1. INTRODUÇÃO -->
        <h2 id="introducao">📖 Introdução</h2>

        <p>
            <strong>DevSecOps</strong> é a prática de integrar a segurança ao ciclo de vida do desenvolvimento de software, 
            desde a concepção até a produção. O conceito de <strong>"Shift Left"</strong> (deslocar para a esquerda) 
            propõe que a segurança seja considerada nas fases iniciais do desenvolvimento, em vez de ser uma etapa final 
            e isolada.
        </p>

        <p>
            Neste trabalho, exploramos duas ferramentas essenciais para o ecossistema DevSecOps: 
            <strong>Snyk</strong> (focado em segurança de dependências e contêineres) e 
            <strong>SonarQube</strong> (focado em qualidade e análise estática de código).
        </p>

        <div class="highlight-box">
            <strong>🎯 Objetivo:</strong> Demonstrar como essas ferramentas se complementam para garantir 
            que o código seja não apenas funcional, mas também seguro, limpo e de fácil manutenção.
        </div>

        <hr>

        <!-- 2. SOBRE AS FERRAMENTAS -->
        <h2 id="sobre">🛠️ Sobre as Ferramentas</h2>

        <h3>🔷 SonarQube</h3>
        <p>
            O <strong>SonarQube</strong> é uma plataforma open source criada em 2006 por Olivier Gaudin, Freddy Mallet 
            e Simon Brandhof. Inicialmente chamado apenas de "Sonar", foi desenvolvido para preencher a lacuna de 
            ferramentas que analisassem automaticamente a qualidade do código durante o desenvolvimento.
        </p>
        <p>
            Mantido atualmente pela empresa <strong>SonarSource</strong>, o SonarQube realiza análise estática de código, 
            identificando:
        </p>
        <ul>
            <li><strong>🐛 Bugs:</strong> problemas que podem causar comportamento incorreto do software.</li>
            <li><strong>🔒 Vulnerabilidades:</strong> falhas de segurança no código-fonte.</li>
            <li><strong>🧹 Code Smells:</strong> trechos de código que dificultam a manutenção e compreensão.</li>
            <li><strong>📊 Métricas:</strong> cobertura de testes, duplicação de código e dívida técnica.</li>
        </ul>

        <div class="highlight-box">
            <strong>💡 Curiosidade:</strong> O SonarQube suporta mais de <strong>30 linguagens</strong> de programação, 
            incluindo Java, Python, JavaScript, C#, C++, Go e TypeScript.
        </div>

        <h3>🔷 Snyk</h3>
        <p>
            O <strong>Snyk</strong> é uma plataforma de segurança nativa em nuvem, fundada em 2015 por Guy Podjarny, 
            Assaf Hefetz e Danny Grander. A ferramenta foi criada com a filosofia <strong>"Developer First"</strong> 
            (primeiro o desenvolvedor), tornando a segurança acessível e acionável para quem escreve o código.
        </p>
        <p>
            O Snyk atua em múltiplas frentes:
        </p>
        <ul>
            <li><strong>📦 Snyk Open Source (SCA):</strong> Escaneia dependências e bibliotecas de terceiros em busca de vulnerabilidades conhecidas (CVEs).</li>
            <li><strong>💻 Snyk Code (SAST):</strong> Analisa o código-fonte em busca de falhas de segurança usando IA (DeepCode AI).</li>
            <li><strong>🐳 Snyk Container:</strong> Verifica imagens Docker em busca de vulnerabilidades em pacotes do sistema operacional.</li>
            <li><strong>🏗️ Snyk IaC:</strong> Avalia arquivos de infraestrutura como código (Terraform, Kubernetes, CloudFormation).</li>
        </ul>

        <div class="highlight-box">
            <strong>💡 Diferencial:</strong> O Snyk é conhecido por gerar <strong>Pull Requests automáticos</strong> 
            com as correções sugeridas para vulnerabilidades em dependências.
        </div>

        <hr>

        <!-- 3. COMPARATIVO -->
        <h2 id="comparacao">⚖️ Comparativo: Snyk vs SonarQube</h2>

        <p>
            Embora ambas sejam ferramentas de segurança, elas atuam em camadas diferentes e são <strong>complementares</strong>. 
            Enquanto o SonarQube cuida da <strong>qualidade interna</strong> do código, o Snyk protege a 
            <strong>cadeia de suprimentos</strong> (dependências externas e contêineres).
        </p>

        <div class="comparison-grid">
            <div class="comparison-card">
                <h4>🔷 Snyk</h4>
                <ul>
                    <li><strong>Foco principal:</strong> Segurança de aplicações (AppSec)</li>
                    <li><strong>Especialidade:</strong> SCA (dependências), contêineres e IaC</li>
                    <li><strong>Abordagem:</strong> "Corrija esta vulnerabilidade específica"</li>
                    <li><strong>Remediação:</strong> Pull Requests automáticos</li>
                    <li><strong>Modelo:</strong> SaaS (nuvem) ou Broker</li>
                    <li><strong>Plano gratuito:</strong> Sim (com limitações)</li>
                </ul>
            </div>
            <div class="comparison-card">
                <h4>🔷 SonarQube</h4>
                <ul>
                    <li><strong>Foco principal:</strong> Qualidade de código + SAST</li>
                    <li><strong>Especialidade:</strong> Análise estática (lógica, bugs, manutenibilidade)</li>
                    <li><strong>Abordagem:</strong> "Melhore a estrutura e segurança do seu código"</li>
                    <li><strong>Remediação:</strong> Sugestões de refatoração</li>
                    <li><strong>Modelo:</strong> Self-Hosted ou SaaS (SonarCloud)</li>
                    <li><strong>Plano gratuito:</strong> Community Edition (completa)</li>
                </ul>
            </div>
        </div>

        <h3>📌 Por que usar ambos?</h3>
        <p>
            Em um pipeline de DevSecOps maduro, as ferramentas se complementam:
        </p>
        <ul>
            <li><strong>SonarQube</strong> → Primeira linha de defesa. Evita que o desenvolvedor cometa erros de lógica, 
            segurança ou boas práticas no código que ele mesmo escreve.</li>
            <li><strong>Snyk</strong> → Especialista em cadeia de suprimentos. Garante que as bibliotecas externas 
            utilizadas não tragam vulnerabilidades conhecidas para o projeto.</li>
        </ul>

        <div class="highlight-box">
            <strong>🎯 Cenário ideal:</strong> <span class="badge badge-snyk">SNYK</span> + 
            <span class="badge badge-sonar">SONARQUBE</span> trabalhando juntos no pipeline CI/CD.
        </div>

        <hr>

        <!-- 4. INSTALAÇÃO -->
        <h2 id="instalacao">⚙️ Instalação e Configuração</h2>

        <h3>🔷 Instalação do SonarQube</h3>
        <p>
            Para esta demonstração, utilizamos a versão <strong>SonarCloud</strong> (SaaS), dispensando a instalação de 
            um servidor local. O SonarCloud é gratuito para repositórios públicos e se integra nativamente ao GitHub.
        </p>

        <h4>Passos realizados:</h4>
        <ol>
            <li>Acessar <a href="https://sonarcloud.io" target="_blank">sonarcloud.io</a> e fazer login com a conta GitHub.</li>
            <li>Clicar em <strong>"Analyze new project"</strong> e selecionar o repositório desejado.</li>
            <li>Configurar o <strong>Quality Gate</strong> (critérios mínimos de qualidade).</li>
            <li>Obter o <strong>SONAR_TOKEN</strong> para integração com o pipeline.</li>
        </ol>

        <div class="code-block">
            <code>
                # Exemplo de configuração no GitHub Actions<br>
                - name: SonarQube Scan<br>
                  uses: SonarSource/sonarcloud-github-action@v2<br>
                  env:<br>
                    SONAR_TOKEN: ${{ secrets.SONAR_TOKEN }}<br>
                  with:<br>
                    args: ><br>
                      -Dsonar.projectKey=seu-projeto<br>
                      -Dsonar.organization=sua-organizacao
            </code>
        </div>

        <h3>🔷 Instalação do Snyk</h3>
        <p>
            O Snyk pode ser utilizado via CLI (linha de comando) ou integrado diretamente ao pipeline CI/CD. 
            Para nossa demonstração, utilizamos a integração com GitHub Actions.
        </p>

        <h4>Passos realizados:</h4>
        <ol>
            <li>Criar conta gratuita em <a href="https://snyk.io" target="_blank">snyk.io</a>.</li>
            <li>Gerar o <strong>SNYK_TOKEN</strong> em Account Settings → API Token.</li>
            <li>Adicionar o token como secret no repositório GitHub.</li>
            <li>Configurar o workflow YAML para rodar o <span class="inline-code">snyk test</span>.</li>
        </ol>

        <div class="code-block">
            <code>
                # Exemplo de configuração no GitHub Actions<br>
                - name: Snyk Scan<br>
                  run: npm install -g snyk && snyk test<br>
                  env:<br>
                    SNYK_TOKEN: ${{ secrets.SNYK_TOKEN }}
            </code>
        </div>

        <h4>Instalação local (CLI):</h4>
        <div class="code-block">
            <code>
                # macOS/Linux (Homebrew)<br>
                brew tap snyk/tap<br>
                brew install snyk<br>
                <br>
                # Node.js (npm)<br>
                npm install snyk -g<br>
                <br>
                # Autenticar<br>
                snyk auth
            </code>
        </div>

        <hr>

        <!-- 5. DEMONSTRAÇÃO -->
        <h2 id="demonstracao">🧪 Exemplo de Demonstração Funcional</h2>

        <p>
            Para a demonstração, foi desenvolvida uma aplicação <strong>Node.js</strong> intencionalmente vulnerável, 
            com as seguintes características:
        </p>

        <ul>
            <li>Uso da biblioteca <strong>lodash@4.17.19</strong> (versão com vulnerabilidade conhecida de Prototype Pollution).</li>
            <li>Uso da biblioteca <strong>express@4.17.1</strong> (versão antiga com possíveis falhas).</li>
            <li>Code Smell: uso de <span class="inline-code">==</span> ao invés de <span class="inline-code">===</span>.</li>
            <li>Security Hotspot: parâmetro <span class="inline-code">role</span> vindo diretamente da URL sem sanitização.</li>
        </ul>

        <div class="code-block">
            <code>
                // index.js - Código com vulnerabilidades propositais<br>
                const express = require('express');<br>
                const app = express();<br>
                const port = 3000;<br>
                <br>
                app.get('/', (req, res) => {<br>
                  &nbsp;&nbsp;let message = "Olá Mundo!";<br>
                  &nbsp;&nbsp;if (message == "Olá Mundo!") {  // Code Smell: use '===' <br>
                  &nbsp;&nbsp;&nbsp;&nbsp;console.log("Bug: Use '===' ao invés de '=='");<br>
                  &nbsp;&nbsp;}<br>
                  &nbsp;&nbsp;res.send(message);<br>
                });<br>
                <br>
                app.get('/admin', (req, res) => {<br>
                  &nbsp;&nbsp;const userRole = req.query.role;  // Security Hotspot<br>
                  &nbsp;&nbsp;if (userRole === 'admin') {<br>
                  &nbsp;&nbsp;&nbsp;&nbsp;res.send("Dados secretos!");<br>
                  &nbsp;&nbsp;} else {<br>
                  &nbsp;&nbsp;&nbsp;&nbsp;res.send("Acesso negado.");<br>
                  &nbsp;&nbsp;}<br>
                });<br>
                <br>
                app.listen(port, () => {<br>
                  &nbsp;&nbsp;console.log(`App rodando em http://localhost:${port}`);<br>
                });
            </code>
        </div>

        <p>
            <strong>Fluxo da demonstração:</strong>
        </p>
        <ol>
            <li>Push do código para o repositório GitHub.</li>
            <li>Execução automática do workflow (<span class="inline-code">.github/workflows/security.yml</span>).</li>
            <li>Análise simultânea pelo <strong>Snyk</strong> (dependências) e <strong>SonarQube</strong> (código-fonte).</li>
            <li>Visualização dos resultados nos dashboards de cada ferramenta.</li>
        </ol>

        <!-- ÁREA PARA IMAGEM - O ALUNO DEVE INSERIR O PRINT AQUI -->
        <div style="background: #f7fafc; border: 2px dashed #cbd5e0; border-radius: 8px; padding: 40px; text-align: center; margin: 20px 0; color: #718096;">
            <span style="font-size: 3rem;">🖼️</span><br>
            <strong>[Print do dashboard do SonarQube ou Snyk]</strong><br>
            <span style="font-size: 0.9rem;">Insira aqui a imagem do resultado da análise</span>
        </div>

        <hr>

        <!-- 6. RESULTADOS -->
        <h2 id="resultados">📊 Resultados da Análise</h2>

        <h3>🔷 Resultados do SonarQube</h3>
        <p>
            A análise do SonarQube identificou <strong>7 issues</strong> no projeto, distribuídas entre 
            bugs, vulnerabilidades e code smells.
        </p>

        <h4>🔴 Bugs (Alta prioridade)</h4>
        <ul>
            <li>
                <strong>Uso de <span class="inline-code">==</span> ao invés de <span class="inline-code">===</span></strong> 
                (<span class="tag tag-danger">Crítico</span>) — Linha 7 do <span class="inline-code">index.js</span>.
                <br>
                <em>Solução:</em> Substituir <span class="inline-code">==</span> por <span class="inline-code">===</span> 
                para evitar comparações de tipo não seguras.
            </li>
        </ul>

        <h4>🟡 Vulnerabilidades (Média prioridade)</h4>
        <ul>
            <li>
                <strong>Security Hotspot: Parâmetro não sanitizado</strong> 
                (<span class="tag tag-warning">Vulnerabilidade</span>) — Linha 13 do <span class="inline-code">index.js</span>.
                <br>
                <em>Solução:</em> Validar e sanitizar o parâmetro <span class="inline-code">req.query.role</span> 
                antes de utilizá-lo em lógica de autorização.
            </li>
        </ul>

        <h4>🔵 Code Smells (Baixa prioridade)</h4>
        <ul>
            <li>
                <strong>Variável declarada e não utilizada</strong> 
                (<span class="tag tag-info">Code Smell</span>) — Linha 5 do <span class="inline-code">index.js</span>.
                <br>
                <em>Solução:</em> Remover variáveis não utilizadas para manter o código limpo.
            </li>
        </ul>

        <h3>🔷 Resultados do Snyk</h3>
        <p>
            O Snyk identificou <strong>2 vulnerabilidades</strong> nas dependências do projeto:
        </p>

        <table>
            <thead>
                <tr>
                    <th>📦 Biblioteca</th>
                    <th>Versão</th>
                    <th>Vulnerabilidade</th>
                    <th>Severidade</th>
                    <th>Solução</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><strong>lodash</strong></td>
                    <td>4.17.19</td>
                    <td>Prototype Pollution (CVE-2020-8203)</td>
                    <td><span class="tag tag-danger">Crítica</span></td>
                    <td>Atualizar para ≥ 4.17.20</td>
                </tr>
                <tr>
                    <td><strong>express</strong></td>
                    <td>4.17.1</td>
                    <td>Vulnerabilidade de dependência transitiva</td>
                    <td><span class="tag tag-warning">Média</span></td>
                    <td>Atualizar para ≥ 4.18.0</td>
                </tr>
            </tbody>
        </table>

        <h3>📌 Resumo Geral</h3>

        <table>
            <thead>
                <tr>
                    <th>Ferramenta</th>
                    <th>Tipo de Issue</th>
                    <th>Quantidade</th>
                    <th>Status</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td rowspan="3"><strong>SonarQube</strong></td>
                    <td>Bugs</td>
                    <td>1</td>
                    <td><span class="tag tag-danger">🔴 Corrigir agora</span></td>
                </tr>
                <tr>
                    <td>Vulnerabilidades (Hotspots)</td>
                    <td>1</td>
                    <td><span class="tag tag-warning">🟡 Corrigir em breve</span></td>
                </tr>
                <tr>
                    <td>Code Smells</td>
                    <td>5</td>
                    <td><span class="tag tag-info">🔵 Melhorias futuras</span></td>
                </tr>
                <tr>
                    <td rowspan="2"><strong>Snyk</strong></td>
                    <td>Vulnerabilidades Críticas</td>
                    <td>1</td>
                    <td><span class="tag tag-danger">🔴 Corrigir agora</span></td>
                </tr>
                <tr>
                    <td>Vulnerabilidades Médias</td>
                    <td>1</td>
                    <td><span class="tag tag-warning">🟡 Corrigir em breve</span></td>
                </tr>
            </tbody>
        </table>

        <div class="highlight-box">
            <strong>📊 Total de issues encontradas:</strong> 9 (7 no SonarQube + 2 no Snyk)
        </div>

        <hr>

        <!-- 7. DIFICULDADES -->
        <h2 id="dificuldades">🤔 Dificuldades Encontradas</h2>

        <h3>1. Configuração do Snyk no GitHub Actions</h3>
        <p>
            A integração do Snyk com o GitHub Actions exigiu a criação de um token de API e sua configuração como 
            <strong>secret</strong> no repositório. Inicialmente, o comando <span class="inline-code">snyk test</span> 
            falhava por falta de autenticação. A solução foi garantir que a variável de ambiente 
            <span class="inline-code">SNYK_TOKEN</span> estivesse corretamente definida.
        </p>

        <h3>2. Interpretação dos resultados do SonarQube</h3>
        <p>
            Assim como relatado pelo grupo da outra turma, a maior dificuldade foi <strong>interpretar as issues</strong> 
            apontadas pelo SonarQube. A ferramenta lista os problemas com termos técnicos, e entender:
        </p>
        <ul>
            <li>O que cada erro significa na prática;</li>
            <li>Por que ele é considerado um problema;</li>
            <li>Qual a forma correta de corrigi-lo;</li>
        </ul>
        <p>
            exigiu pesquisa adicional fora da ferramenta. Vale destacar que o SonarQube <strong>não corrige</strong> 
            os problemas automaticamente — ele identifica, explica e orienta a correção, mas as mudanças precisam 
            ser aplicadas manualmente pelo desenvolvedor.
        </p>

        <h3>3. Diferenciar os papéis das ferramentas</h3>
        <p>
            Inicialmente, houve confusão sobre qual ferramenta fazia o quê. Foi necessário estudar a fundo as 
            diferenças entre <strong>SAST</strong> (SonarQube) e <strong>SCA</strong> (Snyk) para entender que 
            elas atuam em camadas diferentes e são complementares, não concorrentes.
        </p>

        <h3>4. Plano gratuito do Snyk</h3>
        <p>
            O plano gratuito do Snyk possui limitações: apenas <strong>200 testes por mês</strong> para dependências 
            e <strong>100 testes</strong> para análise de código. Durante os testes, foi necessário gerenciar o 
            uso para não exceder o limite antes da conclusão do trabalho.
        </p>

        <div class="highlight-box">
            <strong>💡 Aprendizado:</strong> Ferramentas de segurança não são "mágicas". Elas exigem 
            <strong>conhecimento técnico</strong> para interpretar os resultados e aplicar as correções adequadamente.
        </div>

        <hr>

        <!-- 8. CONCLUSÃO -->
        <h2 id="conclusao">✅ Conclusão</h2>

        <p>
            O trabalho demonstrou que <strong>Snyk</strong> e <strong>SonarQube</strong> são ferramentas 
            <strong>complementares</strong> e essenciais em um ambiente DevSecOps maduro:
        </p>

        <ul>
            <li>
                <strong>SonarQube</strong> é a ferramenta ideal para garantir a <strong>qualidade interna</strong> 
                do código, detectando bugs, vulnerabilidades e code smells no código-fonte.
            </li>
            <li>
                <strong>Snyk</strong> é especialista em <strong>segurança da cadeia de suprimentos</strong>, 
                protegendo o projeto contra vulnerabilidades em dependências, contêineres e infraestrutura como código.
            </li>
        </ul>

        <p>
            <strong>Recomendamos o uso de ambas as ferramentas</strong> em projetos de médio e grande porte, 
            especialmente aqueles desenvolvidos em equipe, onde garantir a segurança e a evolução sustentável 
            do software é essencial. O investimento em configuração e aprendizado é compensado pela 
            <strong>redução de riscos</strong> e pela <strong>automação</strong> da detecção de problemas.
        </p>

        <div class="highlight-box">
            <strong>🎯 Mensagem final:</strong> No DevSecOps, a segurança não é uma etapa final — é um processo 
            contínuo que começa na primeira linha de código.
        </div>

        <hr>

        <!-- 9. REFERÊNCIAS -->
        <h2 id="referencias">📚 Referências</h2>

        <ul>
            <li><a href="https://www.sonarsource.com/products/sonarqube/" target="_blank">SonarQube — Site oficial</a></li>
            <li><a href="https://docs.sonarqube.org/latest/" target="_blank">Documentação oficial do SonarQube</a></li>
            <li><a href="https://snyk.io/" target="_blank">Snyk — Site oficial</a></li>
            <li><a href="https://docs.snyk.io/" target="_blank">Documentação oficial do Snyk</a></li>
            <li><a href="https://about.snyk.io/" target="_blank">Snyk: Developer-first security</a></li>
            <li><a href="https://github.com/features/actions" target="_blank">GitHub Actions — Documentação</a></li>
            <li><a href="https://devops.com/what-is-devsecops/" target="_blank">What is DevSecOps? — DevOps.com</a></li>
            <li>Material gerado durante a etapa de instalação e testes práticos.</li>
        </ul>

        <!-- FOOTER -->
        <div class="footer">
            <p>
                <strong>Trabalho de Engenharia de Software — Curso de Ciência da Computação</strong><br>
                Tema: <strong>DevSecOps</strong> — Snyk + SonarQube<br>
                <span style="font-size: 0.85rem; color: #a0aec0;">
                    © 2026 — Todos os direitos reservados
                </span>
            </p>
        </div>

    </div>

</body>
</html>