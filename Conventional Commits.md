# 🧾 Conventional Commits Guide

Guia rápido e prático de **Conventional Commits** para padronização de commits e consulta no dia a dia.

---

## 📑 Índice

* [Conceito](#conceito)
* [Estrutura do Commit](#estrutura-do-commit)
* [Tipos Principais](#tipos-principais)
* [Tipos Adicionais](#tipos-adicionais)
* [Banco de Dados](#banco-de-dados)
* [Boas Práticas](#boas-práticas)
* [Exemplos](#exemplos)
* [Escopos](#escopos)

---

## 📖 Conceito

A especificação **Conventional Commits** é uma convenção para padronizar mensagens de commit.

Ela ajuda a:

* Organizar o histórico de commits
* Facilitar leitura e manutenção
* Permitir automações (changelog, versionamento, CI/CD)

Também se integra ao padrão de versionamento **SemVer**, indicando:

* novas funcionalidades
* correções
* breaking changes

---

## 🧩 Estrutura do Commit

Formato padrão:

```bash
<tipo>: <descrição curta>
```

### ✔️ Exemplo:

```bash
feat: adicionar autenticação com JWT
```

---

## 🚀 Tipos Principais

| Tipo       | Quando usar                         |
| ---------- | ----------------------------------- |
| `feat`     | Nova funcionalidade                 |
| `fix`      | Correção de bug                     |
| `docs`     | Documentação                        |
| `style`    | Formatação (sem alterar lógica)     |
| `refactor` | Refatoração sem mudar comportamento |
| `test`     | Testes                              |
| `chore`    | Tarefas internas / manutenção       |

---

## ⚙️ Tipos Adicionais

| Tipo       | Quando usar                   |
| ---------- | ----------------------------- |
| `build`    | Build, dependências, ambiente |
| `ci`       | Integração contínua           |
| `perf`     | Melhoria de performance       |
| `revert`   | Reverter commit               |
| `init`     | Commit inicial                |
| `merge`    | Merge de branches             |
| `wip`      | Trabalho em andamento         |
| `hotfix`   | Correção urgente              |
| `config`   | Configurações                 |
| `security` | Correções de segurança        |

---

## 🗄️ Banco de Dados

Padrão recomendado para commits relacionados a banco:

| Situação                          | Tipo    |
| --------------------------------- | ------- |
| Nova estrutura (feature)          | `feat`  |
| Seed / dados iniciais             | `chore` |
| Configuração (Docker, migrations) | `build` |

### ✔️ Exemplos:

```bash
feat: adicionar schema inicial do banco
chore: adicionar seed de dados para testes
build: configurar banco com docker-compose
```

---

## 🧠 Boas Práticas

* Usar mensagens curtas e objetivas
* Começar com verbo no infinitivo
  (ex: adicionar, corrigir, atualizar)
* Evitar commits genéricos:

```bash
update
fix bug
coisas
```

* Preferir:

```bash
fix: corrigir erro na validação de CPF
```

---

## ✨ Exemplos

```bash
feat: adicionar sistema de login
fix: corrigir erro ao salvar usuário
docs: atualizar documentação da API
refactor: melhorar estrutura do serviço de pagamento
test: adicionar testes unitários para autenticação
chore: configurar prettier
build: adicionar suporte a docker
ci: configurar pipeline do GitHub Actions
perf: otimizar consulta no banco de dados
revert: reverter commit de autenticação JWT
```

---

## 🎯 Escopos

Você pode usar **escopos** para maior organização:

```bash
feat(auth): adicionar login com Google
fix(api): corrigir erro no endpoint de usuários
```

