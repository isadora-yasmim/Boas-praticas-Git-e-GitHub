# 🌳 Trunk-Based Development Guide

Guia rápido e prático de **Trunk-Based Development (TBD)** para estudo e consulta no dia a dia.

---

## 📑 Índice

* [Conceito](#-conceito)
* [Estrutura de Branches](#-estrutura-de-branches)
* [Fluxo de Trabalho](#-fluxo-de-trabalho)
* [Feature Flags](#-feature-flags)
* [Integração Contínua](#-integração-contínua-1)
* [Boas Práticas](#-boas-práticas)
* [Quando usar](#%EF%B8%8F-quando-usar)
* [Comparação com Git Flow](#-comparação-com-git-flow)
* [Resumo Rápido](#-resumo-rápido)

---

## 📖 Conceito

**Trunk-Based Development (TBD)** é um modelo de desenvolvimento onde todos os desenvolvedores trabalham em uma única branch principal (geralmente `main`).

A ideia central é:

* Integrar código frequentemente
* Evitar branches longas
* Manter o sistema sempre pronto para deploy

---

## 🌳 Estrutura de Branches

| Branch | Função                                                 |
| ------ | ------------------------------------------------------ |
| `main` | Branch principal (produção + desenvolvimento contínuo) |

---

### 🔸 Branches curtas (opcional)

* `feature/*` (vida curta, poucas horas ou dias)
* Devem ser rapidamente integradas à `main`

---

## 🔄 Fluxo de Trabalho

### 🧩 Desenvolvimento diário

```bash
git checkout main
git pull
git checkout -b feature/minha-feature
```

Após pequenas alterações:

```bash
git add .
git commit -m "feat: adicionar nova funcionalidade"
git push
```

Merge rápido via PR:

```bash
git checkout main
git merge feature/minha-feature
git branch -d feature/minha-feature
```

---

### ⚡ Integração contínua

* Commits frequentes (várias vezes ao dia)
* Integração imediata na `main`
* Testes automatizados obrigatórios

---

## 🚩 Feature Flags

Para evitar quebrar produção:

* Funcionalidades incompletas ficam escondidas
* Ativadas/desativadas via configuração

### ✔️ Exemplo:

```js
if (featureFlagNovaUI) {
  mostrarNovaInterface();
}
```

---

## 🔁 Integração Contínua

No TBD, CI/CD é essencial:

* Build automático a cada commit
* Testes automatizados
* Deploy contínuo (opcional)

Ferramentas comuns:

* GitHub Actions
* GitLab CI
* Jenkins

---

## 📌 Boas Práticas

* Commits pequenos e frequentes
* Não deixar branches abertas por muito tempo
* Sempre manter a `main` estável
* Usar testes automatizados
* Utilizar feature flags para features incompletas

---

## ⚠️ Quando usar

### ✅ Ideal

* Times maduros
* Projetos com CI/CD
* Deploy contínuo
* Alta frequência de entrega

### ❌ Evitar

* Times sem testes automatizados
* Projetos com releases muito formais
* Equipes iniciantes sem disciplina de versionamento

---

## 🔄 Comparação com Git Flow

| Característica      | Git Flow | Trunk-Based |
| ------------------- | -------- | ----------- |
| Branches longas     | Sim      | Não         |
| Complexidade        | Alta     | Baixa       |
| Frequência de merge | Baixa    | Alta        |
| CI/CD               | Opcional | Essencial   |
| Deploy contínuo     | Difícil  | Natural     |

---

## 🧠 Resumo Rápido

```text
main ──●──●──●──●──●──●──●──●──
         ↑  ↑  ↑  ↑  ↑
       commits frequentes
```

* Uma única branch principal
* Integração constante
* Feedback rápido

