# 💼 Projeto de Automação - SauceDemo com Cypress

Este projeto automatiza o fluxo de compra no site [SauceDemo](https://www.saucedemo.com/) utilizando **Cypress** com **JavaScript**.

---

## 📌 Funcionalidades testadas

- Login com usuário válido
- Login com senha incorreta
- Login com usuário bloqueado
- Adição de produto ao carrinho
- Validação da quantidade no carrinho
- Início do processo de checkout

---

## 🧪 Como executar os testes

### Pré-requisitos

- Node.js instalado (v18+)
- Git instalado

### Passos para rodar localmente

```bash
# Clone o repositório
git clone https://github.com/juliojacob1979/saucedemo-cypress.git
cd saucedemo-cypress

# Instale as dependências
npm install

# Execute os testes em modo CLI
npx cypress run

# Ou execute no modo interativo (GUI)
npx cypress open
```

---

## ⚙️ Integração Contínua (CI)

Este projeto utiliza **GitHub Actions** para executar os testes automaticamente a cada `push` ou `pull request` na branch `main`.

O arquivo de pipeline está em: `.github/workflows/run-cypress-tests.yml`

---

## 🚀 Tecnologias

- [Cypress](https://www.cypress.io/)
- [GitHub Actions](https://github.com/features/actions)

---

## 👤 Autor

Julio Fonseca Jacob  
[https://github.com/juliojacob1979](https://github.com/juliojacob1979)