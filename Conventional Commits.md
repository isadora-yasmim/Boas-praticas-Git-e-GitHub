# 📌 Guia - Conventional Commits

A especificação [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) é uma convenção leve para padronizar mensagens de commit. Ela define um conjunto simples de regras que tornam o histórico de alterações mais claro e organizado, facilitando a criação de ferramentas automatizadas. Além disso, se integra ao versionamento semântico (SemVer), ao descrever nas mensagens as novas funcionalidades, correções e mudanças que quebram compatibilidade.

---

## 🧩 Estrutura do commit

```
<tipo>: <descrição curta>
```

### ✔️ Exemplo:

```
feat: adicionar autenticação com JWT
```

---

## 🚀 Tipos principais

| Tipo         | Quando usar                         |
| ------------ | ----------------------------------- |
| **feat**     | Nova funcionalidade                 |
| **fix**      | Correção de bug                     |
| **docs**     | Documentação                        |
| **style**    | Formatação (sem alterar lógica)     |
| **refactor** | Refatoração sem mudar comportamento |
| **test**     | Testes                              |
| **chore**    | Tarefas internas / manutenção       |

---

## ⚙️ Tipos adicionais

| Tipo         | Quando usar                                   |
| ------------ | --------------------------------------------- |
| **build**    | Build, dependências, configuração de ambiente |
| **ci**       | Integração contínua (GitHub Actions, etc.)    |
| **perf**     | Melhoria de performance                       |
| **revert**   | Reverter commit                               |
| **init**     | Commit inicial do projeto                     |
| **merge**    | Merge de branches                             |
| **wip**      | Work in progress (trabalho em andamento)      |
| **hotfix**   | Correção urgente em produção                  |
| **config**   | Alterações em arquivos de configuração        |
| **security** | Correções de segurança                        |

---

## 🗄️ Banco de dados (padrão recomendado)

| Situação                          | Tipo    |
| --------------------------------- | ------- |
| Nova estrutura de banco (feature) | `feat`  |
| Dump/seed inicial                 | `chore` |
| Configuração (Docker, migrations) | `build` |

### ✔️ Exemplos:

```
feat: adicionar schema inicial do banco
chore: adicionar seed de dados para testes
build: configurar banco com docker-compose
```

---

## 🧠 Boas práticas

✔ Use frases curtas e objetivas
✔ Comece com verbo no infinitivo (ex: adicionar, corrigir, atualizar)
✔ Evite commits genéricos como:

```
update
fix bug
coisas
```

✔ Prefira:

```
fix: corrigir erro na validação de CPF
```

---

## ✨ Exemplos completos

```
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

## 🎯 Dica extra 

Você pode usar **escopos** para deixar ainda mais organizado:

```
feat(auth): adicionar login com Google
fix(api): corrigir erro no endpoint de usuários
```

