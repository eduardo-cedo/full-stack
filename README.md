# full-stack

Este é um guia prático para você dominar o fluxo de trabalho entre o seu computador (local) e o GitHub (remoto). O Git funciona em camadas, e entender esse movimento é a chave para não se perder.

---

## 🏗️ 1. Configuração Inicial

Antes de começar, você precisa se identificar para o Git. Isso dará a autoria aos seus commits.

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu-email@exemplo.com"

---

## 🚀 2. Iniciando um Projeto

Você tem dois caminhos: começar do zero ou baixar algo que já existe.

* **`git init`**: Transforma a pasta atual em um repositório Git.
* **`git clone <url-do-repositorio>`**: Cria uma cópia local de um projeto que já está no GitHub.

---

## 🔄 3. O Ciclo de Trabalho (Local)

O fluxo básico consiste em três estágios: o diretório de arquivos, a área de preparação (staging) e o repositório.

1. **`git status`**: O comando mais importante. Ele diz o que foi modificado e o que está pronto para ser salvo.
2. **`git add <arquivo>`**: Adiciona um arquivo específico para a "fila" de salvamento.
* *Dica:* Use `git add .` para adicionar todas as mudanças de uma vez.


3. **`git commit -m "descrição da mudança"`**: Grava as alterações permanentemente no seu histórico local.

---

## ☁️ 4. Sincronizando com o GitHub

Agora que você salvou localmente, precisa enviar para a nuvem.

* **`git remote add origin <url-do-github>`**: Conecta seu código local ao repositório no GitHub (só precisa fazer uma vez).
* **`git push -u origin main`**: Envia seus commits para o GitHub. (O `-u` configura o destino padrão para os próximos envios).
* **`git pull`**: Traz as novidades que seus colegas enviaram para o GitHub para o seu computador.

---

## 🌿 5. Trabalhando com Branches (Ramos)

Branches permitem que você crie uma "linha do tempo paralela" para testar novos recursos sem estragar a versão principal do código.

* **`git branch <nome-da-branch>`**: Cria um novo ramo.
* **`git checkout <nome-da-branch>`**: Muda para o ramo criado.
* **`git checkout -b <nome-da-branch>`**: Atalho que cria e já muda para o novo ramo ao mesmo tempo.
* **`git merge <nome>`**: Traz as alterações do ramo `<nome>` para o ramo onde você está agora.

---

## 🛠️ 6. Comandos de Inspeção e Segurança

* **`git log --oneline`**: Mostra o histórico de commits de forma resumida.
* **`git diff`**: Mostra exatamente quais linhas você mudou antes de fazer o `add`.
* **`git checkout -- <arquivo>`**: Descarta as mudanças feitas em um arquivo e volta ele ao estado original.

---

## 💡 Resumo do Fluxo Diário

Na prática, o seu dia a dia será quase sempre este:

1. `git pull` (para atualizar seu código)
2. *Trabalha no código...*
3. `git status` (para ver o que mudou)
4. `git add .` (para preparar as mudanças)
5. `git commit -m "Explicação do que fiz"` (para salvar)
6. `git push` (para enviar ao GitHub)