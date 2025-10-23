# 🍺 Sistema de Controle de Produção e Vendas - Cervejaria BeboSim

> **Disciplina:** Engenharia de Software  
> **Professor:** Radamés Pereira  
> **Instituição:** Universidade Comunitária da Região de Chapecó (UNOCHAPECÓ)  
> **Período:** 2025

---

## 📋 Índice

1. [Introdução](#-1-introdução)
2. [Descrição Geral](#-2-descrição-geral)
3. [Princípios Ágeis Aplicados](#-3-princípios-ágeis-aplicados)
4. [Gerência de Configuração de Software](#%EF%B8%8F-4-gerência-de-configuração-de-software-gcs)
5. [Requisitos Específicos](#-5-requisitos-específicos)
6. [Arquitetura do Sistema](#%EF%B8%8F-6-arquitetura-do-sistema)
7. [Como Contribuir](#-7-como-contribuir)
8. [Autor](#-8-autor)
9. [Licença](#-9-licença)

---

## 🎯 1. Introdução

### 1.1. Propósito

Este documento especifica o **Sistema de Controle de Produção e Vendas** para a Cervejaria BeboSim, desenvolvido como projeto prático da disciplina de Engenharia de Software. O sistema visa otimizar os processos de negócio da cervejaria, melhorando a gestão de estoque, produção, vendas e campanhas publicitárias através de uma solução integrada e eficiente.

### 1.2. Escopo do Projeto

O sistema abrangerá o cadastro e gerenciamento completo de:

- 🍻 **Produtos Líquidos**
  - Cerveja branca e escura
  - Guaraná normal e light
  - Água mineral com e sem gás
  - Controle de estoque, preços e fórmulas de produção

- 🏭 **Unidades de Produção**
  - Cadastro de fábricas (nome, endereço, CNPJ, área construída)
  - Associação de produtos por unidade de produção
  - Controle de capacidade produtiva

- 📦 **Embalagens**
  - Garrafas plásticas de diversos tamanhos
  - Garrafas de vidro
  - Latas de alumínio de diferentes capacidades
  - Controle de custos e volumes suportados

- 👥 **Equipes de Vendas e Pessoal**
  - Cadastro de vendedores e gerentes
  - Controle de regiões atendidas
  - Histórico de alocação em equipes
  - Gestão de comissões

- 🏢 **Clientes (Pessoas Jurídicas)**
  - Razão social, CNPJ, endereço
  - Telefone e pessoa de contato
  - Histórico de compras

- 💰 **Pedidos de Venda**
  - Número do pedido, data de emissão
  - Vendedor responsável e cliente
  - Quantidades de produtos vendidos

- 📢 **Campanhas Publicitárias**
  - Nome, datas de início e término
  - Produtos participantes e preços promocionais
  - Garoto/garota-propaganda
  - Investimento previsto e retorno estimado

### 1.3. Definições, Acrônimos e Abreviações

| Termo | Definição |
|-------|-----------|
| **GCS** | Gerência de Configuração de Software |
| **IEEE** | Institute of Electrical and Electronics Engineers |
| **PO** | Product Owner (Proprietário do Produto) |
| **SM** | Scrum Master |
| **CI/CD** | Continuous Integration / Continuous Deployment |
| **SCV** | Sistema de Controle de Versão |
| **PR** | Pull Request |
| **SCMP** | Sistema de Compra de Matéria Prima |
| **SCL** | Sistema de Compra de Lanches |

---

## 🧩 2. Descrição Geral

### 2.1. Perspectiva do Produto

O sistema será uma **aplicação web moderna e responsiva**, acessível através de navegadores em desktops e dispositivos móveis. Ele integrará os processos existentes da Cervejaria BeboSim, substituindo controles manuais e planilhas por uma plataforma centralizada e automatizada.

**Características principais:**
- Interface responsiva e intuitiva
- Acesso via navegadores web (Chrome, Firefox, Edge, Safari)
- Integração com banco de dados MySQL
- Arquitetura modular e escalável

### 2.2. Funções do Produto

| Módulo | Funcionalidades Principais |
|--------|---------------------------|
| **Gestão de Produção** | • Cadastro de produtos e fórmulas<br>• Controle de unidades de produção<br>• Gerenciamento de estoque<br>• Associação produto-fábrica |
| **Gestão de Vendas** | • Cadastro de equipes e vendedores<br>• Registro de clientes<br>• Emissão de pedidos<br>• Cálculo de comissões |
| **Gestão de Campanhas** | • Cadastro de campanhas publicitárias<br>• Controle de preços promocionais<br>• Análise de retorno sobre investimento<br>• Acompanhamento de desempenho |
| **Relatórios Gerenciais** | • Relatórios de vendas por período<br>• Análise de produção<br>• Indicadores de desempenho<br>• Controle de comissões |

### 2.3. Características dos Usuários

| Tipo de Usuário | Perfil | Responsabilidades |
|-----------------|--------|-------------------|
| **Gerente-Geral** | Acesso completo ao sistema | Visualização de todos os módulos e relatórios estratégicos |
| **Gerente de Produção** | Foco em operações industriais | Gerenciamento de produtos, fórmulas e unidades de produção |
| **Gerente de Vendas** | Foco em comercialização | Administração de equipes, vendedores e análise de desempenho |
| **Vendedor** | Usuário operacional | Cadastro de clientes e emissão de pedidos de venda |

### 2.4. Restrições

- O sistema deve ser desenvolvido utilizando **tecnologias web modernas e responsivas**
- O acesso será controlado por **níveis de permissão** baseados no perfil do usuário
- Deve garantir a **integridade, segurança e confidencialidade** dos dados
- Conformidade com a **Lei Geral de Proteção de Dados (LGPD)**
- Código versionado e auditável via **Git/GitHub**

### 2.5. Hipóteses de Trabalho

**Plataforma de Desenvolvimento:**
- **Linguagens:** Python, JavaScript, Ruby
- **Frameworks:** Django (Python), React (JavaScript), Ruby on Rails
- **Banco de Dados:** MySQL para produção
- **IDEs:** Visual Studio Code, RubyMine, Jupyter Notebook
- **Hardware:** Computador com 16-32 GB RAM, 256GB SSD, processador i7

**Plataforma de Operação:**
- **Desktop:** Windows 10, macOS, Ubuntu Linux
- **Mobile:** Android, iOS
- **Servidores:** Linux Ubuntu Server em nuvem (AWS)
- **Navegadores:** Chrome, Firefox, Edge, Safari

---

## 🌀 3. Princípios Ágeis Aplicados

O desenvolvimento do sistema segue os **valores e princípios do Manifesto Ágil**, promovendo flexibilidade, entregas contínuas e colaboração com stakeholders.

### 3.1. Valores Ágeis no Projeto

| Valor do Manifesto Ágil | Aplicação no Projeto BeboSim |
|--------------------------|------------------------------|
| **Indivíduos e interações** mais que processos e ferramentas | • Comunicação direta entre equipe e stakeholders<br>• Daily Scrums para alinhamento<br>• Workshops colaborativos |
| **Software funcionando** mais que documentação abrangente | • Entregas incrementais de módulos funcionais<br>• Feedback contínuo do gerente da BeboSim<br>• Demonstrações ao final de cada Sprint |
| **Colaboração com o cliente** mais que negociação de contratos | • Participação ativa dos gestores da BeboSim<br>• Priorização conjunta de funcionalidades<br>• Sprint Reviews com stakeholders |
| **Responder a mudanças** mais que seguir um plano | • Product Backlog flexível e adaptável<br>• Ajustes baseados em feedback<br>• Capacidade de incorporar novos requisitos |

### 3.2. Práticas Ágeis Adotadas

#### 🎯 Papéis Definidos

- **Product Owner (PO):** Leonardo Pereira
- **Desenvolvedor** Leonardo Pereira
- **Scrum Master:** Leonardo Pereira

#### 📅 Ciclo de Desenvolvimento

```
┌─────────────────────────────────────────────────────────────┐
│  Sprint Planning (2h)                                        │
│  → Definição de objetivos e seleção de itens do backlog     │
└─────────────────────────────────────────────────────────────┘
                            ↓
┌─────────────────────────────────────────────────────────────┐
│  Sprint (2 semanas)                                          │
│  → Daily Scrums (15min)                                      │
│  → Desenvolvimento incremental                               │
│  → Integração contínua                                       │
└─────────────────────────────────────────────────────────────┘
                            ↓
┌─────────────────────────────────────────────────────────────┐
│  Sprint Review (1h)                                          │
│  → Demonstração do software funcionando                      │
│  → Coleta de feedback dos stakeholders                       │
└─────────────────────────────────────────────────────────────┘
                            ↓
┌─────────────────────────────────────────────────────────────┐
│  Sprint Retrospective (1h)                                   │
│  → Análise de melhorias                                      │
│  → Ajustes para próximos Sprints                             │
└─────────────────────────────────────────────────────────────┘
```

#### 📊 Product Backlog Inicial (Priorizado)

1. **[ALTA] Módulo de Cadastro de Produtos**
   - Cadastrar produtos com nome, estoque, preço, comissão e fórmula
   - Visualizar lista de produtos cadastrados
   - Editar e excluir produtos

2. **[ALTA] Módulo de Gestão de Unidades de Produção**
   - Cadastrar fábricas com dados completos
   - Associar produtos às unidades de produção
   - Visualizar produtos por fábrica

3. **[MÉDIA] Módulo de Gestão de Embalagens**
   - Cadastrar tipos de embalagens
   - Associar embalagens a produtos
   - Controlar custos por embalagem

4. **[MÉDIA] Módulo de Equipes de Vendas**
   - Cadastrar vendedores e gerentes
   - Gerenciar regiões atendidas
   - Manter histórico de alocações

5. **[BAIXA] Módulo de Campanhas Publicitárias**
   - Criar e gerenciar campanhas
   - Definir preços promocionais
   - Analisar ROI de campanhas

---

## ⚙️ 4. Gerência de Configuração de Software (GCS)

A **GCS** é fundamental para garantir a rastreabilidade, integridade e controle sobre todos os artefatos do projeto ao longo de seu ciclo de vida.

### 4.1. Conceitos Fundamentais

| Conceito | Descrição | Aplicação no Projeto |
|----------|-----------|---------------------|
| **Item de Configuração** | Qualquer artefato sob controle de GCS | Código-fonte, documentos, requisitos, testes, fórmulas de produção |
| **Linha de Base (Baseline)** | Versão formalmente aprovada | Aprovação de requisitos iniciais ou versão funcional do sistema |
| **Sistema de Controle de Versão** | Ferramenta para gerenciar versões | Git como SCV distribuído |
| **Controle de Mudanças** | Processo formal para mudanças | Issues e Pull Requests no GitHub |
| **Auditoria de Configuração** | Verificação de conformidade | Revisão de código e testes automatizados |

### 4.2. Práticas de GCS com Git e GitHub

#### 🌳 Modelo de Branching (GitFlow Simplificado)

```
main (produção)
  ↑
  └── develop (desenvolvimento)
        ↑
        ├── feature/cadastro-produtos
        ├── feature/gestao-vendas
        ├── feature/campanhas
        └── hotfix/correcao-urgente
```

**Branches principais:**
- `main`: código em produção, sempre estável
- `develop`: branch de desenvolvimento, integração de features

**Branches de suporte:**
- `feature/*`: desenvolvimento de novas funcionalidades
- `hotfix/*`: correções urgentes em produção
- `release/*`: preparação de novas versões

#### 🔄 Fluxo de Trabalho

1. **Criar feature branch** a partir de `develop`
   ```bash
   git checkout develop
   git checkout -b feature/nome-da-funcionalidade
   ```

2. **Desenvolver e commitar** com mensagens descritivas
   ```bash
   git add .
   git commit -m "feat: adiciona cadastro de produtos"
   ```

3. **Push para repositório remoto**
   ```bash
   git push origin feature/nome-da-funcionalidade
   ```

4. **Abrir Pull Request** para revisão

5. **Após aprovação, merge** em `develop`

6. **Quando estável, merge** de `develop` em `main`

#### 📝 Convenção de Commits

Seguimos o padrão **Conventional Commits**:

```
<tipo>(<escopo>): <descrição curta>

<corpo opcional>

<rodapé opcional>
```

**Tipos:**
- `feat`: nova funcionalidade
- `fix`: correção de bug
- `docs`: alteração em documentação
- `style`: formatação de código
- `refactor`: refatoração sem mudança de comportamento
- `test`: adição ou correção de testes
- `chore`: tarefas de manutenção

**Exemplos:**
```
feat(produtos): adiciona CRUD de produtos
fix(vendas): corrige cálculo de comissões
docs(readme): atualiza instruções de instalação
```

### 4.3. Controle de Qualidade

#### ✅ Revisão de Código (Code Review)

- Todo código deve passar por **Pull Request**
- Mínimo de **1 aprovação** antes do merge
- Verificação de:
  - Aderência aos padrões de codificação
  - Cobertura de testes
  - Documentação adequada
  - Ausência de bugs evidentes

#### 🤖 Integração Contínua (CI)

Através do **GitHub Actions**, automatizamos:
- Execução de testes unitários
- Análise estática de código
- Build do projeto
- Verificação de vulnerabilidades

**Exemplo de workflow:**
```yaml
name: CI

on: [push, pull_request]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Run tests
        run: |
          npm install
          npm test
```

---

## 📋 5. Requisitos Específicos

### 5.1. Requisitos Funcionais Principais

**R1.0** - Obter o valor faturado no dia  
**R1.1** - Melhorar a eficiência e precisão do atendimento ao cliente  
**R1.2** - Consultar o cardápio de produtos disponíveis  
**R1.3** - Realizar pedido e efetuar pagamento  
**R1.4** - Otimizar comunicação entre atendentes, caixa e cozinha  
**R1.5** - Integrar com a cozinha para preparação ágil  
**R1.6** - Permitir acompanhamento do status do pedido  
**R1.7** - Obter informações de compra de matéria prima  
**R1.8** - Proporcionar experiência de compra agradável  
**R1.9** - Facilitar gerenciamento interno do estabelecimento  
**R1.10** - Controlar consumo de matéria prima  
**R1.11** - Conhecer o número de clientes atendidos  
**R1.12** - Conhecer quantos e quais produtos foram entregues

### 5.2. Requisitos Não-Funcionais

#### Desempenho
- Tempo de resposta inferior a 2 segundos para consultas
- Suporte a 100 usuários simultâneos

#### Segurança
- Autenticação e autorização baseada em papéis
- Criptografia de dados sensíveis
- Conformidade com LGPD

#### Usabilidade
- Interface intuitiva e responsiva
- Compatibilidade com principais navegadores
- Acessibilidade (WCAG 2.1 nível AA)

#### Confiabilidade
- Disponibilidade de 99.5%
- Backup diário automatizado
- Recuperação de desastres

---

## 🏗️ 6. Arquitetura do Sistema

### 6.1. Visão Geral

O sistema seguirá uma arquitetura em camadas:

```
┌─────────────────────────────────────┐
│   Camada de Apresentação            │
│   (React / Interface Web)           │
└─────────────────────────────────────┘
              ↕
┌─────────────────────────────────────┐
│   Camada de Aplicação                │
│   (Django / Ruby on Rails)          │
└─────────────────────────────────────┘
              ↕
┌─────────────────────────────────────┐
│   Camada de Negócio                  │
│   (Lógica de Negócio)               │
└─────────────────────────────────────┘
              ↕
┌─────────────────────────────────────┐
│   Camada de Dados                    │
│   (MySQL)                           │
└─────────────────────────────────────┘
```

### 6.2. Tecnologias Utilizadas

- **Frontend:** React, HTML5, CSS3, JavaScript ES6+
- **Backend:** Django (Python) ou Ruby on Rails
- **Banco de Dados:** MySQL 8.0+
- **Controle de Versão:** Git + GitHub
- **CI/CD:** GitHub Actions
- **Containerização:** Docker (futuro)

### 6.3. Diagramas

Diagramas UML detalhados (Casos de Uso, Classes, Sequência, Atividades) serão disponibilizados na **Wiki do repositório**.

---

## 🤝 7. Como Contribuir

Este é um projeto educacional, mas seguimos boas práticas de colaboração:

### 7.1. Fluxo de Contribuição

1. **Fork** o repositório
2. **Clone** para sua máquina local
   ```bash
   git clone https://github.com/LeonardoLPX/es2025-cervejaria-bebosim.git
   ```
3. **Crie uma branch** para sua feature
   ```bash
   git checkout -b feature/minha-feature
   ```
4. **Commit** suas alterações
   ```bash
   git commit -m "feat: adiciona minha feature"
   ```
5. **Push** para o GitHub
   ```bash
   git push origin feature/minha-feature
   ```
6. **Abra um Pull Request** descrevendo suas mudanças

### 7.2. Padrões de Código

- Seguir PEP 8 (Python) ou Ruby Style Guide
- Escrever testes para novas funcionalidades
- Documentar código complexo
- Manter commits pequenos e focados

---

## 👤 8. Autor

**Leonardo Pereira**  
📧 E-mail: [leonardo13@unochapeco.edu.br](mailto:leonardo13@unochapeco.edu.br)  
🐙 GitHub: [@LeonardoLPX](https://github.com/LeonardoLPX)  

**Orientador:**  
Prof. Radamés Pereira  
📧 E-mail: [radames@unochapeco.edu.br](mailto:radames@unochapeco.edu.br)

---

## 📄 9. Licença

Este projeto está licenciado sob a **Licença MIT**.

```
MIT License

Copyright (c) 2025 Leonardo Pereira

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 📚 Referências

1. **Manifesto para Desenvolvimento Ágil de Software**  
   https://agilemanifesto.org/iso/ptbr/manifesto.html

2. **Pressman, R. S. (2011)**  
   *Engenharia de Software: Uma Abordagem Profissional*. 7ª ed. McGraw-Hill

3. **Chacon, S., & Straub, B. (2014)**  
   *Pro Git* (2nd ed.). Apress. https://git-scm.com/book/en/v2

4. **IEEE Std 830-1998**  
   *IEEE Recommended Practice for Software Requirements Specifications*

5. **IEEE Std 828-2012**  
   *Configuration Management in Systems and Software Engineering*

---

<div align="center">

**🍺 Desenvolvido com dedicação para a Cervejaria BeboSim 🍺**

*Engenharia de Software • UNOCHAPECÓ • 2025*

</div>