# 🧭 Git Flow Guide

Guia rápido e prático de **Git Flow** para estudo e consulta no dia a dia.

---

## 📑 Índice

* [📖 Conceito](#-conceito)
* [🌳 Estrutura de Branches](#-estrutura-de-branches)
* [🔄 Fluxo de Trabalho](#-fluxo-de-trabalho)
* [🏷️ Versionamento](#-versionamento)
* [📌 Boas Práticas](#-boas-práticas)
* [⚠️ Quando usar](#️-quando-usar)
* [🔁 Alternativas](#-alternativas)
* [🧠 Resumo Rápido](#-resumo-rápido)

---

## 📖 Conceito

O **Git Flow** é um modelo de organização de branches que define padrões claros para desenvolvimento, releases e correções.

Ele ajuda a:

* Organizar o trabalho em equipe
* Separar desenvolvimento de produção
* Facilitar manutenção e versionamento

---

## 🌳 Estrutura de Branches

### 🔹 Principais

| Branch    | Função                        |
| --------- | ----------------------------- |
| `main`    | Produção (código estável)     |
| `develop` | Integração de funcionalidades |

---

### 🔸 Suporte

| Tipo        | Origem  | Uso                   |
| ----------- | ------- | --------------------- |
| `feature/*` | develop | Novas funcionalidades |
| `release/*` | develop | Preparação de versão  |
| `hotfix/*`  | main    | Correções urgentes    |

---

## 🔄 Fluxo de Trabalho

### 🧩 Feature

```bash
git checkout develop
git checkout -b feature/nova-feature
```

Finalizar:

```bash
git checkout develop
git merge feature/nova-feature
git branch -d feature/nova-feature
```

---

### 🚀 Release

```bash
git checkout develop
git checkout -b release/v1.0.0
```

Finalizar:

```bash
git checkout main
git merge release/v1.0.0

git checkout develop
git merge release/v1.0.0

git branch -d release/v1.0.0
```

---

### 🔥 Hotfix

```bash
git checkout main
git checkout -b hotfix/correcao
```

Finalizar:

```bash
git checkout main
git merge hotfix/correcao

git checkout develop
git merge hotfix/correcao

git branch -d hotfix/correcao
```

---

## 🏷️ Versionamento

Padrão **SemVer**:

```
MAJOR.MINOR.PATCH
```

| Tipo  | Quando usar                      |
| ----- | -------------------------------- |
| MAJOR | Mudanças quebram compatibilidade |
| MINOR | Nova funcionalidade              |
| PATCH | Correção de bugs                 |

Exemplo:

```
v1.2.3
```

---

## 📌 Boas Práticas

* Não commitar direto na `main`
* Sempre usar Pull Request
* Nomear branches de forma clara
* Fazer commits pequenos e descritivos
* Revisar código antes de merge

---

## ⚠️ Quando usar

### ✅ Ideal

* Projetos médios/grandes
* Times com vários devs
* Releases planejadas

### ❌ Evitar

* Projetos pequenos
* Deploy contínuo (CI/CD intenso)
* Times muito reduzidos

---

## 🔁 Alternativas

* GitHub Flow
* GitLab Flow
* Trunk-Based Development

---

## 🧠 Resumo Rápido

```
main ───────────────●──────────────●────────
                     \            /
develop ─────●───────●───────●───────●─────
              \       \       \
feature       ●       ●       ●

release               ●──────●

hotfix        ●──────●
```


