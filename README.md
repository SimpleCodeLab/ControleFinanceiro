# 💰 ControleFinanceiro

Aplicação desenvolvida com o objetivo de auxiliar no controle de receitas, despesas e organização financeira pessoal.

---

## 📋 Índice

- [Sobre o Projeto](#-sobre-o-projeto)
- [Estrutura do Projeto](#-estrutura-do-projeto)
- [Padrões de Projeto](#-padrões-de-projeto)
- [Como Contribuir](#-como-contribuir)
- [Fluxo de Branches](#-fluxo-de-branches)
- [Dicionário Git & GitHub](#-dicionário-git--github)
- [Contribuidores](#-contribuidores)

---

## 📖 Sobre o Projeto

O **ControleFinanceiro** é uma aplicação que tem como objetivo auxiliar usuários no controle de suas finanças pessoais. Com ela é possível registrar receitas e despesas, categorizá-las e acompanhar relatórios para uma melhor organização financeira.

---

## 🗂️ Estrutura do Projeto

O projeto segue uma arquitetura modular, onde cada funcionalidade principal é isolada em seu próprio módulo, facilitando a manutenção e escalabilidade.

```
ControleFinanceiro/
│
├── src/                        # Código-fonte principal da aplicação
│   ├── modules/                # Módulos de funcionalidades
│   │   ├── autenticacao/       # Cadastro, login e controle de sessão do usuário
│   │   ├── receitas/           # Registro e gerenciamento de receitas (entradas)
│   │   ├── despesas/           # Registro e gerenciamento de despesas (saídas)
│   │   ├── relatorios/         # Geração de relatórios e resumos financeiros
│   │   └── categorias/         # Categorias para classificar receitas e despesas
│   │
│   ├── shared/                 # Recursos compartilhados entre módulos
│   │   ├── components/         # Componentes reutilizáveis (UI, formulários, etc.)
│   │   └── utils/              # Funções utilitárias e helpers genéricos
│   │
│   └── config/                 # Configurações globais da aplicação (env, rotas, etc.)
│
├── docs/                       # Documentação técnica do projeto
├── tests/                      # Testes automatizados
└── README.md                   # Este arquivo
```

### Resumo dos Módulos

| Módulo | Descrição |
|---|---|
| `autenticacao` | Responsável pelo cadastro, login, logout e controle de sessão dos usuários |
| `receitas` | Gerencia o registro, edição e exclusão de entradas financeiras (salário, freelance, etc.) |
| `despesas` | Gerencia o registro, edição e exclusão de saídas financeiras (contas, compras, etc.) |
| `relatorios` | Gera resumos, gráficos e exportações com base nas receitas e despesas cadastradas |
| `categorias` | Permite criar e gerenciar categorias para organizar melhor as movimentações |
| `shared/components` | Componentes de interface reutilizáveis em toda a aplicação |
| `shared/utils` | Funções auxiliares (formatação de moeda, datas, validações, etc.) |
| `config` | Centraliza configurações como variáveis de ambiente, temas e rotas da aplicação |

---

## 🏗️ Padrões de Projeto

> 🚧 **Seção em construção** — Esta seção será preenchida conforme o projeto evoluir.

Aqui serão documentados os padrões de projeto, convenções de código e boas práticas adotadas pela equipe, como:

- Padrão de nomenclatura de arquivos e variáveis
- Padrão de commits (ex: Conventional Commits)
- Arquitetura adotada (MVC, Clean Architecture, etc.)
- Guia de estilo de código

---

## 🤝 Como Contribuir

Obrigado por querer contribuir com o **ControleFinanceiro**! Siga os passos abaixo:

### 1. Faça um Fork do repositório

Clique em **Fork** no canto superior direito da página do repositório no GitHub.

### 2. Clone o seu Fork localmente

```bash
git clone https://github.com/SEU-USUARIO/ControleFinanceiro.git
cd ControleFinanceiro
```

### 3. Crie uma branch para a sua feature

```bash
git checkout dev
git pull origin dev
git checkout -b feature/nome-da-sua-feature
```

### 4. Faça suas alterações e commit

```bash
git add .
git commit -m "feat: descrição curta do que foi feito"
```

### 5. Envie sua branch para o GitHub

```bash
git push origin feature/nome-da-sua-feature
```

### 6. Abra um Pull Request

No GitHub, abra um **Pull Request** da sua branch `feature/nome-da-sua-feature` para a branch `dev` do repositório original. Descreva claramente o que foi feito.

> ⚠️ **Nunca abra Pull Requests direto para a `main`.**

---

## 🌿 Fluxo de Branches

Utilizamos um fluxo de branches simples para organizar o desenvolvimento e garantir a estabilidade do código em produção.

```
main
 └── dev
      └── feature/nome-da-feature
```

### `main` — Versão Estável

- Representa o código que está **em produção** (funcionando e estável).
- **Nunca** faça commits ou push direto nessa branch.
- Apenas recebe merges vindos da `dev`, após revisão e aprovação.

### `dev` — Integração

- Branch de **desenvolvimento e integração** de novas funcionalidades.
- Aqui as features prontas são reunidas e testadas em conjunto antes de ir para produção.
- Ao terminar sua feature, abra um Pull Request da sua branch para a `dev`.

### `feature/nome-da-feature` — Desenvolvimento Individual

- Cada desenvolvedor cria sua própria branch a partir da `dev` para trabalhar em uma funcionalidade específica.
- Exemplo: `feature/tela-de-login`, `feature/cadastro-de-despesas`.
- Ao concluir, abra um Pull Request para a `dev`.

### Resumo do Fluxo

```
1. Crie sua branch: git checkout -b feature/minha-feature (a partir de dev)
2. Desenvolva e faça commits
3. Abra PR: feature/minha-feature → dev
4. Após revisão, a feature é mergeada na dev
5. Quando a dev estiver estável, ela é mergeada na main
```

---

## 📚 Dicionário Git & GitHub

Um glossário rápido para facilitar o dia a dia de quem está começando.

### Git

| Termo | Significado |
|---|---|
| **Repositório (repo)** | Pasta do projeto controlada pelo Git, que guarda todo o histórico de alterações |
| **Commit** | Um "salvar" com mensagem descritiva; registra as alterações feitas no código |
| **Branch** | Uma ramificação independente do código; permite desenvolver sem afetar a versão principal |
| **Merge** | Unir as alterações de uma branch com outra |
| **Clone** | Copiar um repositório remoto para a sua máquina local |
| **Pull** | Baixar e aplicar as últimas alterações do repositório remoto na sua branch local |
| **Push** | Enviar seus commits locais para o repositório remoto |
| **Fetch** | Baixar as atualizações do repositório remoto sem aplicar automaticamente |
| **Checkout** | Trocar de branch ou restaurar arquivos para um estado anterior |
| **Stage / Add** | Marcar arquivos para incluir no próximo commit (`git add`) |
| **Stash** | Guardar temporariamente alterações não commitadas para continuar depois |
| **Rebase** | Reorganizar commits de uma branch sobre outra (alternativa ao merge) |
| **Conflict** | Conflito: quando duas branches alteram o mesmo trecho de código e o Git não sabe qual manter |
| **Log** | Histórico de commits (`git log`) |
| **.gitignore** | Arquivo que lista o que o Git deve ignorar (ex: `node_modules`, `.env`) |

### GitHub

| Termo | Significado |
|---|---|
| **GitHub** | Plataforma online que hospeda repositórios Git e facilita a colaboração em equipe |
| **Fork** | Cópia de um repositório para a sua própria conta no GitHub |
| **Pull Request (PR)** | Solicitação para que suas alterações sejam revisadas e incorporadas a outra branch |
| **Issue** | Registro de um bug, sugestão ou tarefa a ser feita no projeto |
| **Review** | Revisão de código feita por outro desenvolvedor antes de aprovar um PR |
| **Merge PR** | Ação de aceitar e integrar o Pull Request na branch de destino |
| **Actions** | Ferramenta do GitHub para automatizar tarefas como testes e deploys (CI/CD) |
| **README** | Arquivo de apresentação e documentação do projeto (este arquivo!) |
| **Release** | Versão "empacotada" e publicada do projeto |
| **Star** | Forma de favoritar e mostrar interesse em um repositório |
| **Clone vs Fork** | Clone: cópia local do repositório. Fork: cópia do repositório na sua conta GitHub |

---

## 👥 Contribuidores

> 🚧 **Seção em construção** — Aqui serão listados os desenvolvedores e colaboradores do projeto.

<!-- 
Exemplo de formato:

| Nome | GitHub | Papel |
|------|--------|-------|
| Fulano de Tal | [@fulano](https://github.com/fulano) | Desenvolvedor |
-->
