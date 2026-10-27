# Front-End – Sistema de Gestão de Pessoas

**Atividade 08 – Consumindo o Back-End no Front-End – CRUD**

**Professor:** Vitor Lima Santana  
**Aluno(a):** João Vittor Neves de sales  
**Disciplina:** Programação Back-End

## 1. Objetivo

Desenvolver uma aplicação Front-End utilizando HTML, CSS e JavaScript para consumir uma API REST desenvolvida em Node.js, Express e MySQL/MariaDB.

A atividade tem como foco implementar o cadastro de pessoas utilizando o método HTTP **POST**, a função `fetch()` e o tratamento de erros com `async/await` e `try/catch`.

## 2. Tecnologias utilizadas

- HTML5
- CSS3
- JavaScript
- Fetch API
- Async/Await
- Try/Catch
- Node.js e Express (Back-End)
- MySQL/MariaDB (Banco de dados)

## 3. Estrutura do projeto

```text
frontend-gestao-pessoas/
│
├── index.html
├── cadastro.html
├── editar.html
│
├── css/
│   └── style.css
│
├── js/
│   ├── listar.js
│   ├── cadastro.js
│   └── editar.js
│
└── README.md
```

## 4. Funcionalidades

O sistema possui as seguintes operações:

| Método | Rota | Funcionalidade |
|---|---|---|
| GET | /pessoas | Listar pessoas |
| GET | /pessoas/:id | Consultar pessoa |
| POST | /pessoas | Cadastrar pessoa |
| PUT | /pessoas/:id | Atualizar pessoa |
| DELETE | /pessoas/:id | Excluir pessoa |

## 5. Implementação do POST

O aluno deverá desenvolver o arquivo `js/cadastro.js`, responsável por capturar os dados do formulário HTML e enviá-los para a API.

A implementação deverá utilizar:

- `addEventListener("submit", ...)`
- `preventDefault()`
- `async/await`
- `try/catch`
- `fetch()`
- `method: "POST"`
- `JSON.stringify()`
- Verificação de `resposta.ok`

### Exemplo da estrutura de requisição

```javascript
const resposta = await fetch(
  "http://localhost:3000/pessoas",
  {
    method: "POST",
    headers: {
      "Content-Type": "application/json"
    },
    body: JSON.stringify({
      nome,
      idade
    })
  }
);
```

O código deverá estar dentro de uma função assíncrona, com tratamento de erros utilizando `try/catch`.

O aluno também deverá validar os campos nome e idade antes de enviar os dados.

## 6. Como executar

### Back-End

1. Realizar o Fork do repositório original disponibilizado pelo professor.
2. Clonar o repositório.
3. Instalar as dependências:

```bash
npm install
```

4. Configurar a conexão com o banco de dados.
5. Iniciar a API:

```bash
npm start
```

A API estará disponível em:

`http://localhost:3000`

### Front-End

1. Abrir o projeto no Visual Studio Code.
2. Verificar se o Back-End está funcionando.
3. Executar `index.html` com o Live Server.
4. Acessar a página de cadastro.
5. Cadastrar uma pessoa.
6. Verificar se os dados foram armazenados no banco de dados.

## 7. Evidências

Adicione capturas de tela demonstrando:

**Imagem 1 – Tela de listagem**

![alt text](<images/Captura de tela 2026-10-22 165528.png>)

**Imagem 2 – Formulário de cadastro**

![alt text](<images/Captura de tela 2026-10-22 165608.png>)

**Imagem 3 – Cadastro funcionando**

![alt text](<images/Captura de tela 2026-10-27 130809.png>)

**Imagem 4 – Registro inserido no banco de dados**

![alt text](<images/Captura de tela 2026-10-27 115525.png>)

## 8. Repositórios

**Back-End (Fork):** https://github.com/joaovsales-byte/ProjetoFullStack

**Front-End:** https://github.com/joaovsales-byte/ProjetoFullStack2

## 9. Conclusão do aluno

Explique com suas palavras:

- Como funciona a comunicação entre o Front-End e o Back-End?
* O Front-End é a parte visual do sistema, onde o usuário interage. Ele envia requisições ao Back-End, que processa as informações e se comunica com o banco de dados. Depois, o Back-End retorna uma resposta ao Front-End.

- Qual é a finalidade do método POST?
* O método POST serve para enviar e cadastrar novos dados no sistema. Por exemplo, na API de tarefas, ele permite cadastrar uma nova tarefa no banco de dados.

- Por que utilizamos `async/await` e `try/catch`?
* O async/await permite trabalhar com operações assíncronas, como consultas ao banco de dados, sem precisar bloquear o restante do código. Já o try/catch permite tratar erros que podem acontecer durante a execução, evitando que problemas interrompam o funcionamento esperado do sistema.

- Quais dificuldades você encontrou durante a atividade?
* Encontrei dificuldades na hora de conectar o Back-End com o Front-End e fazwe com que o cadastro e edição funcionassem.

    Concluí que a atividade me ajudou a entender melhor como funciona a comunicação entre o Front-End e o Back-End. Tive dificuldades para conectar as duas partes e fazer com que as funções de cadastro e edição funcionassem corretamente, mas consegui aprender mais sobre requisições HTTP, consumo de APIs e tratamento de erros com JavaScript. Essa experiência foi importante para aprimorar meus conhecimentos em desenvolvimento web e entender melhor como criar sistemas que se comunicam com um banco de dados.

---

## Créditos

**Professor responsável:** Vitor Lima Santana

**Desenvolvido por:** João Vittor Neves de sales

**Atividade 08 – Desenvolvimento Web e Consumo de APIs REST**