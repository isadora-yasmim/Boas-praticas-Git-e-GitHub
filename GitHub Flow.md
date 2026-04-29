# 🌿 GitHub Flow 

O **GitHub Flow** é um modelo de fluxo de trabalho simples, moderno e amplamente utilizado por times ágeis. Ele é ideal para projetos com entregas contínuas e deploy frequente.

## 📑 Índice

- [📌 O que é GitHub Flow](#-o-que-é-github-flow)
- [🚀 Quando usar](#-quando-usar)
- [🌳 Estrutura do fluxo](#-estrutura-do-fluxo)
- [🔄 Passo a passo completo](#-passo-a-passo-completo)
- [💡 Boas práticas](#-boas-práticas)
- [⚠️ Erros comuns](#️-erros-comuns)
- [🆚 GitHub Flow vs Git Flow](#-github-flow-vs-git-flow)
- [📌 Resumo visual](#-resumo-visual)


## 📌 O que é GitHub Flow

O **GitHub Flow** é um fluxo de trabalho baseado em:

- Uma única branch principal (`main`)
- Criação de branches curtas para cada tarefa
- Integração contínua via Pull Requests
- Deploy frequente (às vezes várias vezes ao dia)

👉 Ele prioriza **simplicidade, velocidade e colaboração**.


## 🚀 Quando usar

Use GitHub Flow quando:

- 🔹 O projeto precisa de deploy contínuo
- 🔹 O time trabalha com metodologias ágeis
- 🔹 As mudanças são pequenas e frequentes
- 🔹 Existe CI/CD configurado

❌ Evite quando:
- Há múltiplas versões em produção simultaneamente
- O projeto exige controle rígido de releases


## 🌳 Estrutura do fluxo

```

main
├── feature/login
├── fix/header-bug
└── feature/payment

````

- `main` → sempre estável e pronta para produção
- branches → curtas, específicas e descartáveis


## 🔄 Passo a passo completo

### 1. Criar uma branch

```bash
git checkout -b feature/nome-da-feature
````

📌 Sempre crie a partir da `main` atualizada.


### 2. Desenvolver a funcionalidade

```bash
git add .
git commit -m "feat: adiciona tela de login"
```

💡 Commits pequenos e bem descritos.


### 3. Enviar para o repositório remoto

```bash
git push origin feature/nome-da-feature
```


### 4. Abrir um Pull Request (PR)

No GitHub:

* Explique o que foi feito
* Descreva o problema resolvido
* Adicione prints (se necessário)


### 5. Revisão de código (Code Review)

* Outros devs analisam o código
* Sugestões e melhorias são feitas
* Ajustes podem ser solicitados


### 6. Merge na `main`

Após aprovação:

```bash
Merge Pull Request
```


### 7. Deploy

* Deploy automático (CI/CD) ou manual
* A `main` deve estar sempre pronta para produção


### 8. Deletar a branch

```bash
git branch -d feature/nome-da-feature
```

ou pelo GitHub.


## 💡 Boas práticas

✔ Use nomes descritivos:

```
feature/login
fix/navbar-bug
hotfix/payment-error
```

✔ Faça commits seguindo padrão:

```
feat: nova funcionalidade
fix: correção de bug
docs: atualização de documentação
```

✔ Mantenha PRs pequenos
✔ Sempre atualize sua branch com a `main`
✔ Use CI/CD para validação automática


## ⚠️ Erros comuns

❌ Branches muito grandes
❌ PRs difíceis de revisar
❌ Commits genéricos ("update", "fix")
❌ Não revisar código
❌ Deixar a `main` quebrada


## 🆚 GitHub Flow vs Git Flow

| Critério     | GitHub Flow 🌿  | Git Flow 🌳         |
| ------------ | --------------- | ------------------- |
| Complexidade | Baixa           | Alta                |
| Branches     | Poucas          | Muitas              |
| Deploy       | Contínuo        | Baseado em releases |
| Ideal para   | Startups / SaaS | Sistemas complexos  |
| Velocidade   | Alta            | Média               |


## 📌 Resumo visual

```
1. Criar branch
        ↓
2. Desenvolver
        ↓
3. Commitar
        ↓
4. Push
        ↓
5. Pull Request
        ↓
6. Review
        ↓
7. Merge na main
        ↓
8. Deploy 🚀
```


## ✨ Conclusão

O **GitHub Flow** é perfeito para times modernos que buscam:

* 🚀 Velocidade
* 🤝 Colaboração
* 🔄 Entrega contínua

Se bem aplicado, ele reduz complexidade e aumenta produtividade.

💡 **Dica final:**
```
Combine GitHub Flow com **CI/CD + testes automatizados** para alcançar nível profissional.
```


