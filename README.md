# Gerenciador de Tarefas

Este é um projeto de um **gerenciador de tarefas** criado com Vue.js e JavaScript, com uma estrutura modular para facilitar a manutenção e expansão do código. O objetivo principal do projeto é fornecer uma interface simples para criar, editar e excluir tarefas, permitindo que os usuários organizem suas atividades de forma prática.

## Funcionalidades

- **Adicionar Tarefa**: O usuário pode adicionar novas tarefas, especificando o tipo (pessoal ou profissional) e o conteúdo da tarefa.
- **Listar Tarefas**: As tarefas são listadas de forma clara, exibindo seu status (concluída ou pendente) e opções para edição e exclusão.
- **Marcar como Concluída**: O usuário pode marcar uma tarefa como concluída, alterando a cor e adicionando uma linha sobre o texto.
- **Editar e Excluir**: Cada tarefa possui botões de edição e exclusão para facilitar o gerenciamento.
- **Filtro de Tarefas**: As tarefas podem ser filtradas para exibir apenas as pendentes ou concluídas.
## Pré-requisitos

Antes de começar, certifique-se de ter os seguintes softwares instalados em sua máquina:

- **Node.js**: É necessário para executar o projeto Vue.js.
  - Faça o download do Node.js na [página oficial](https://nodejs.org/) e instale-o.
  - Após a instalação, verifique se o Node.js foi instalado corretamente executando o comando abaixo no terminal:
    ```bash
    node -v
    ```
  - Este comando deve exibir a versão do Node.js instalada. 

- **npm (Node Package Manager)**: Geralmente, o npm é instalado automaticamente junto com o Node.js.
  - Verifique se o npm está instalado com o comando:
    ```bash
    npm -v
    ```
  - Isso deve exibir a versão do npm. Se não estiver disponível, instale o npm separadamente.

## Como Rodar o Projeto

Siga os passos abaixo para configurar e rodar o projeto localmente.

### 1. Clone o Repositório

Clone este repositório para o seu computador:
```bash
git clone https://github.com/seu-usuario/gerenciador-de-tarefas.git
```

### 2. Acesse o Diretório do Projeto
Navegue até o diretório do projeto:
```bash
    cd gerenciador-de-tarefas
```

### 3. Instale as Dependências
Instale as dependências do projeto utilizando o npm:
```bash
    npm install
```

### 4. Inicie o Servidor de Desenvolvimento
Após instalar as dependências, inicie o servidor de desenvolvimento:

```bash
npm run serve
```

Este comando vai iniciar o servidor local e fornecer um link, geralmente http://localhost:8080, onde você pode visualizar o projeto no navegador.

## Construção para Produção
Para criar uma versão de produção otimizada, execute:

```bash
npm run build
```
## Stack utilizada

**Front-end:** Vue.js
