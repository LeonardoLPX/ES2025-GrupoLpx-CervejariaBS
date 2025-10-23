# Checklist de Instalação e Configuração do Git e GitHub para Windows (Iniciante)

Este guia passo a passo foi elaborado para **iniciantes** que utilizam o sistema operacional **Windows**. Ele cobre a instalação do Git, a criação de uma conta no GitHub e a configuração inicial necessária para começar a desenvolver projetos de software.

---

## 1. Instalação do Git no Windows

O Git é a ferramenta de controle de versão que você instala localmente em seu computador.

| Passo | Ação | Instruções Detalhadas | Links Necessários |
| :---: | :--- | :--- | :--- |
| **1.1** | **Download do Instalador** | Acesse o site oficial do Git para Windows e clique no botão de download. O download começará automaticamente. | [Git for Windows](https://gitforwindows.org/) |
| **1.2** | **Execução do Instalador** | Localize o arquivo baixado (`.exe`) e clique duas vezes para iniciar o assistente de instalação. | |
| **1.3** | **Configurações Iniciais** | Na maioria das telas, você pode clicar em **"Next"** (Próximo) mantendo as opções padrão. **Para iniciantes, é recomendado:** | |
| | | - **"Adjusting your PATH environment"**: Selecionar **"Git from the command line and also from 3rd-party software"** (A opção do meio). | |
| | | - **"Choosing the default editor used by Git"**: Manter o editor padrão (geralmente o Vim) ou selecionar um de sua preferência (como o VS Code, se já estiver instalado). | |
| | | - **"Choosing the default branch name"**: Selecionar **"Let Git decide"** ou **"Override the default branch name for new repositories"** e digitar `main`. | |
| **1.4** | **Conclusão** | Clique em **"Install"** (Instalar) e, ao finalizar, desmarque a opção **"View Release Notes"** e clique em **"Finish"** (Concluir). | |
| **1.5** | **Verificação da Instalação** | Abra o **"Git Bash"** (procure no menu Iniciar) ou o **Prompt de Comando/PowerShell** e digite o comando abaixo: | |
| | | ```bash
git --version
``` | |
| | | O resultado deve mostrar a versão do Git instalada, confirmando o sucesso da instalação. | |

---

## 2. Criação da Conta no GitHub

O GitHub é a plataforma online que armazena seus projetos (repositórios) na nuvem.

| Passo | Ação | Instruções Detalhadas | Links Necessários |
| :---: | :--- | :--- | :--- |
| **2.1** | **Acesso ao Site** | Acesse a página de cadastro do GitHub. | [Página de Cadastro do GitHub](https://github.com/signup) |
| **2.2** | **Preenchimento dos Dados** | Siga as instruções na tela, fornecendo: | |
| | | - Seu **endereço de e-mail**. | |
| | | - Uma **senha** segura. | |
| | | - Um **nome de usuário** único. | |
| **2.3** | **Verificação e Confirmação** | Complete o desafio de segurança (captcha) e, em seguida, verifique sua conta através do link enviado para o seu e-mail. | |
| **2.4** | **Configuração do Perfil** | Preencha as informações adicionais sobre seu perfil e preferências. | |

---

## 3. Configuração Inicial do Git (Local)

Após a instalação, você precisa informar ao Git quem você é para que seus commits (registros de alterações) sejam corretamente identificados.

| Passo | Ação | Instruções Detalhadas | Comandos Necessários |
| :---: | :--- | :--- | :--- |
| **3.1** | **Abrir o Terminal** | Abra o **Git Bash** (recomendado no Windows) ou o Prompt de Comando/PowerShell. | |
| **3.2** | **Configurar Nome de Usuário** | Digite o comando abaixo, substituindo `"Seu Nome Completo"` pelo nome que deseja que apareça em seus commits. | ```bash
git config --global user.name "Seu Nome Completo"
``` |
| **3.3** | **Configurar E-mail** | Digite o comando abaixo, substituindo `seu.email@exemplo.com` pelo **mesmo e-mail** que você usou para criar sua conta no GitHub. | ```bash
git config --global user.email seu.email@exemplo.com
``` |
| **3.4** | **Verificar Configurações** | Para garantir que tudo foi configurado corretamente, use o comando: | ```bash
git config --list
``` |
| | | Você deve ver `user.name` e `user.email` com os valores que você definiu. | |

---

## 4. Conexão Segura (SSH ou HTTPS)

Para que seu computador possa enviar e receber dados do GitHub, é preciso estabelecer uma conexão segura. Para iniciantes, a forma mais simples é usar o protocolo **HTTPS** com o **Gerenciador de Credenciais do Git**.

| Passo | Ação | Instruções Detalhadas | Comandos/Links Necessários |
| :---: | :--- | :--- | :--- |
| **4.1** | **Clonar um Repositório (Primeira Vez)** | Na primeira vez que você tentar interagir com um repositório remoto (por exemplo, clonar um projeto do GitHub), o Git irá solicitar suas credenciais. | |
| **4.2** | **Autenticação** | O Git para Windows usará o **Git Credential Manager (GCM)**. Uma janela de login do GitHub será aberta. | |
| **4.3** | **Login** | Faça login com seu nome de usuário e senha do GitHub. O GCM irá armazenar essas credenciais de forma segura no Windows, e você não precisará digitá-las novamente por um longo período. | [Mais sobre o Git Credential Manager](https://docs.github.com/pt/get-started/getting-started-with-git/caching-your-github-credentials-in-git) |

---

## 5. Próximos Passos (Comandos Essenciais)

Com o Git instalado e configurado, e a conta do GitHub criada, você está pronto para iniciar seu primeiro projeto!

| Comando | Descrição | Exemplo de Uso |
| :--- | :--- | :--- |
| `git init` | Inicializa um novo repositório Git no diretório atual. | `git init` |
| `git add .` | Adiciona todos os arquivos modificados ao "staging area" (área de preparação). | `git add .` |
| `git commit -m "Mensagem"` | Salva as alterações permanentemente no histórico local do Git. | `git commit -m "Primeiro commit do projeto"` |
| `git remote add origin URL` | Conecta seu repositório local a um repositório remoto (no GitHub). | `git remote add origin https://github.com/usuario/projeto.git` |
| `git push -u origin main` | Envia os commits locais para o repositório remoto no GitHub. | `git push -u origin main` |
| `git pull origin main` | Baixa e mescla as alterações do repositório remoto para o seu repositório local. | `git pull origin main` |
| `git clone URL` | Cria uma cópia local de um repositório que já existe no GitHub. | `git clone https://github.com/usuario/projeto.git` |

---

**Referências:**

[1] Git for Windows. Disponível em: [https://gitforwindows.org/](https://gitforwindows.org/)
[2] Página de Cadastro do GitHub. Disponível em: [https://github.com/signup](https://github.com/signup)
[3] Caching your GitHub credentials in Git. Disponível em: [https://docs.github.com/pt/get-started/getting-started-with-git/caching-your-github-credentials-in-git](https://docs.github.com/pt/get-started/getting-started-with-git/caching-your-github-credentials-in-git)

