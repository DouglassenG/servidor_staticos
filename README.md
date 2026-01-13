# 🌐 Servidor de Arquivos Estáticos

![Status](https://img.shields.io/badge/Status-Operacional-green)
![NodeJS](https://img.shields.io/badge/Runtime-Node.js-green?logo=node.js&logoColor=white)
![Grunt](https://img.shields.io/badge/Tool-Grunt-fba919?logo=grunt&logoColor=white)
![HTTP](https://img.shields.io/badge/Protocol-HTTP-blue)

> Uma implementação leve de servidor HTTP local para desenvolvimento Frontend, eliminando barreiras de testes com arquivos estáticos.

## 🎯 Motivação e Propósito

Desenvolver abrindo arquivos diretamente no navegador (protocolo `file://`) gera comportamentos inconsistentes, especialmente ao lidar com caminhos de imagens, fontes e requisições AJAX (bloqueio de CORS).

O propósito deste repositório é fornecer um **Ambiente de Desenvolvimento Local** robusto. Ele resolve esses problemas levantando uma instância de servidor HTTP, simulando fielmente como a aplicação se comportará quando estiver online em produção.

## 🛠️ Tecnologias Utilizadas

A infraestrutura do projeto utiliza o ecossistema Node.js:

* **[Node.js](https://nodejs.org/):** Runtime JavaScript para execução do servidor.
* **[Grunt.js](https://gruntjs.com/):** Task Runner utilizado para configurar e rodar o serviço.
* **[grunt-contrib-connect](https://github.com/gruntjs/grunt-contrib-connect):** Plugin middleware responsável por criar o servidor web estático.

## ✨ Funcionalidades

O projeto está configurado para entregar:

1.  **Servidor HTTP:** Disponibiliza os arquivos do projeto em uma porta local (ex: `localhost:8080`).
2.  **Live Reload (Opcional/Configurável):** Permite a atualização automática do navegador ao salvar alterações no código.
3.  **Mapeamento de Diretório:** Define a pasta raiz (`root`) de onde os arquivos devem ser lidos, garantindo a integridade dos caminhos.

## 📦 Instalação e Configuração

Este projeto roda sobre o Node.js. Siga os passos para configurar o ambiente.

### Pré-requisitos
* **Node.js** e **NPM** instalados.
* **Git** instalado.

### Passo a Passo

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/DouglassenG/servidor_staticos.git](https://github.com/DouglassenG/servidor_staticos.git)
    ```

2.  **Acesse o diretório:**
    ```bash
    cd servidor_staticos
    ```

3.  **Instale as dependências:**
    O comando abaixo lerá o arquivo `package.json` e instalará o Grunt e o plugin `grunt-contrib-connect`.
    ```bash
    npm install
    ```

4.  **Inicie o Servidor:**
    Para levantar a aplicação localmente:
    ```bash
    npm run grunt
    # Ou via CLI global:
    grunt
    ```

## 💻 Uso e Exemplos

Após executar o comando de inicialização, o terminal indicará que o servidor está rodando e "aguardando" (Keepalive).

**Saída esperada no terminal:**
```text
Running "connect:server" (connect) task
Started connect web server on http://localhost:8080
