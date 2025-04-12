# 💼 Projeto de Automação - SauceDemo com Cypress

Este projeto automatiza o fluxo de compra no site [SauceDemo](https://www.saucedemo.com/) utilizando **Cypress** com **JavaScript**.

---

## 🧑‍💻 História do Usuário

**Como** cliente da SauceDemo,  
**quero** poder acessar minha conta, navegar pelos produtos, adicioná-los ao carrinho e finalizar a compra,  
**para que** eu possa fazer minhas compras com praticidade e segurança.

---

## ✅ Critérios de Aceite

- O login deve funcionar com usuários válidos e falhar com credenciais incorretas ou usuários bloqueados.  
- O usuário deve conseguir adicionar produtos ao carrinho.  
- O carrinho deve refletir corretamente a quantidade de produtos adicionados.  
- O fluxo de checkout deve estar acessível após o login e a adição de produtos ao carrinho.  
- Mensagens de erro devem ser exibidas corretamente em caso de falha no login.

---

## 🧪 Casos de Teste

| CT   | Descrição                                 | Pré-condição             | Resultado Esperado                                      |
|------|-------------------------------------------|--------------------------|----------------------------------------------------------|
| CT01 | Login com usuário válido                  | Acesso à página de login | Redirecionar para `/inventory.html`                     |
| CT02 | Login com senha inválida                  | Acesso à página de login | Exibir mensagem de erro de login inválido               |
| CT03 | Login com usuário bloqueado               | Acesso à página de login | Exibir mensagem informando que o usuário está bloqueado |
| CT04 | Adicionar produto ao carrinho             | Usuário autenticado      | Badge do carrinho com número "1"                        |
| CT05 | Validar produto no carrinho               | Produto adicionado       | Carrinho com o item correto                             |
| CT06 | Iniciar processo de checkout              | Produto no carrinho      | Redirecionar para `/checkout-step-one.html`            |

---

## ⏱️ Estimativa de Tempo de Teste

| Tipo                      | Tempo por Execução | Nº de Casos | Total Estimado |
|--------------------------|--------------------|-------------|----------------|
| Execução Manual          | ~2 minutos         | 6           | ~12 minutos    |
| Execução com Cypress     | ~5 segundos        | 6           | ~30 segundos   |

**Ganho estimado com automação:** ~96% de redução no tempo

---

## 🧠 Justificativa dos Testes Automatizados

Foram priorizados testes nos principais fluxos críticos do sistema:

- Login (válido e inválido)  
- Comportamento do carrinho de compras  
- Início do fluxo de checkout  

Esses fluxos representam as ações principais de um usuário real e ajudam a garantir estabilidade nas entregas contínuas com CI/CD.

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
