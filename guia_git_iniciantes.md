# 🐙 Guia de Git para Iniciantes
### Aprenda a versionar seus projetos do zero!

---

## O que é o Git?

Imagina que você está escrevendo um trabalho escolar no computador. Você salva, continua editando, aí percebe que apagou algo importante e não tem como voltar atrás. 😱

O **Git** resolve exatamente isso! Ele é um sistema que **salva "fotos" do seu projeto ao longo do tempo**, permitindo que você volte para qualquer versão quando quiser. E o melhor: dá pra trabalhar em equipe sem sobrescrever o trabalho de ninguém!

O **GitHub** é um site onde você guarda esses projetos na nuvem, podendo acessá-los de qualquer lugar.

---

## ⚙️ Configurando o ambiente no Windows

Antes de usar o Git, você precisa instalar e dizer para ele **quem você é**. Assim, quando você salvar algo no GitHub, ele vai saber que foi você!

### Passo 1 — Instale o Git

Acesse **https://git-scm.com**, baixe o instalador para Windows e execute-o. Pode deixar todas as opções no padrão e clicar em "Next" até finalizar.

### Passo 2 — Abra o terminal

Pressione `Windows + R`, digite `cmd` e pressione Enter. Você também pode usar o **Git Bash**, que vem instalado junto com o Git.

### Passo 3 — Diga ao Git quem você é

Digite os comandos abaixo, substituindo pelos **seus dados do GitHub**:

```bash
git config --global user.name "Seu Nome Aqui"
git config --global user.email "seu@email.com"
```

> 💡 Use o **mesmo e-mail** cadastrado na sua conta do GitHub! Isso é o que liga seus commits à sua conta.

### Passo 4 — Configure o acesso ao GitHub (Token)

O GitHub não aceita mais senha comum pelo terminal. Você precisa de um **Token de Acesso Pessoal**. Siga os passos:

1. Acesse **github.com** e faça login
2. Clique na sua foto → **Settings**
3. No menu lateral, clique em **Developer settings**
4. Clique em **Personal access tokens** → **Tokens (classic)**
5. Clique em **Generate new token (classic)**
6. Dê um nome, selecione a opção **repo** e clique em **Generate token**
7. **Copie o token gerado** (ele só aparece uma vez!)

Na primeira vez que você fizer um `git push`, o Windows vai pedir seu usuário e senha. No campo de senha, **cole o token** no lugar da senha normal. O Windows vai guardar essa informação automaticamente para os próximos acessos.

### Passo 5 — Verifique se tudo está certo

```bash
git config --list
```

Você deve ver seu nome e e-mail listados. Pronto, ambiente configurado! 🎉

---

## 📚 Comandos do Git — Do básico ao avançado

---

### 1. `git init` — Iniciar um repositório

```bash
git init
```

**O que faz:** Transforma uma pasta comum em um repositório Git. É o primeiro comando que você usa quando começa um projeto novo.

> 💡 Pense nisso como "ligar a câmera" antes de começar a tirar fotos do seu projeto.

---

### 2. `git clone` — Copiar um projeto do GitHub

```bash
git clone https://github.com/usuario/nome-do-repositorio.git
```

**O que faz:** Baixa um projeto que já existe no GitHub para o seu computador, já pronto para usar com Git.

> 💡 É como baixar um jogo: você pega a versão completa e já pode jogar (ou no caso, programar)!

---

### 3. `git status` — Ver o que mudou

```bash
git status
```

**O que faz:** Mostra quais arquivos foram modificados, criados ou deletados desde o último salvamento. Você vai usar isso o tempo todo!

> 💡 É como olhar no espelho antes de sair: você vê o que está diferente.

---

### 4. `git add` — Selecionar o que vai ser salvo

```bash
# Adicionar um arquivo específico
git add nome-do-arquivo.txt

# Adicionar TODOS os arquivos modificados de uma vez
git add .
```

**O que faz:** Coloca os arquivos na "fila" para serem salvos. No Git, você escolhe exatamente o que quer incluir no próximo salvamento.

> 💡 Imagina que você vai tirar uma foto em grupo. O `git add` é o momento de chamar as pessoas que vão aparecer na foto.

---

### 5. `git commit` — Salvar uma versão do projeto

```bash
git commit -m "Descrição do que foi feito"
```

**O que faz:** Tira a "foto" dos arquivos que você adicionou com `git add` e salva com uma mensagem explicando o que mudou.

> 💡 A mensagem entre aspas é muito importante! Escreva algo que faça sentido, como `"Adicionei a tela de login"` ou `"Corrigi o bug do botão"`. Isso ajuda você e sua equipe a entenderem o histórico.

---

### 6. `git log` — Ver o histórico de versões

```bash
# Histórico completo
git log

# Histórico resumido, uma linha por commit
git log --oneline
```

**O que faz:** Mostra todas as "fotos" (commits) que foram tiradas do projeto, com data, autor e mensagem.

> 💡 É como abrir o álbum de fotos do seu projeto e ver tudo que já aconteceu.

---

### 7. `git diff` — Ver exatamente o que mudou

```bash
git diff
```

**O que faz:** Mostra linha por linha o que foi alterado nos arquivos desde o último commit. Linhas em verde (+) foram adicionadas, linhas em vermelho (-) foram removidas.

> 💡 Útil quando você quer revisar suas mudanças antes de fazer o commit.

---

### 8. `git branch` — Trabalhar em paralelo

```bash
# Ver as branches existentes
git branch

# Criar uma nova branch
git branch nome-da-branch

# Trocar para outra branch
git checkout nome-da-branch

# Criar e já trocar para a nova branch (atalho!)
git checkout -b nome-da-branch
```

**O que faz:** Uma **branch** é como uma "linha do tempo paralela" do seu projeto. Você pode criar uma para testar algo novo sem bagunçar o projeto principal.

> 💡 Pense em um jogo com vários slots de save. A branch principal (`main`) é o jogo original, e você pode criar outras para experimentar sem perder o progresso principal.

---

### 9. `git merge` — Juntar branches

```bash
git merge nome-da-branch
```

**O que faz:** Junta as mudanças de uma branch com a branch atual. Use quando terminar de desenvolver uma funcionalidade nova e quiser colocá-la no projeto principal.

> 💡 É como pegar as anotações do caderno de rascunho e passar para o caderno principal depois de revisar.

---

### 10. `git remote` — Conectar ao GitHub

```bash
# Ver os repositórios remotos conectados
git remote -v

# Conectar seu projeto local ao GitHub
git remote add origin https://github.com/usuario/repositorio.git
```

**O que faz:** Liga o seu projeto local (no computador) a um repositório no GitHub (na nuvem). O apelido `origin` é o nome padrão usado para o repositório remoto principal.

> 💡 É como adicionar um contato no celular: você dá um nome ("origin") para um endereço longo.

---

### 11. `git push` — Enviar para o GitHub

```bash
# Enviar a branch atual
git push origin nome-da-branch

# Na primeira vez, use -u para definir o padrão:
git push -u origin main
```

**O que faz:** Envia seus commits do computador para o GitHub. Assim outras pessoas (ou você em outro computador) podem ver e baixar suas mudanças.

> 💡 É como publicar uma foto no Instagram: você tira a foto (commit) e depois posta (push) para o mundo ver.

---

### 12. `git pull` — Baixar atualizações do GitHub

```bash
git pull origin main
```

**O que faz:** Baixa as mudanças mais recentes do GitHub e já aplica no seu projeto local. Sempre faça isso antes de começar a trabalhar para não ficar desatualizado!

> 💡 É como dar aquela atualizada no WhatsApp para ver as mensagens que chegaram enquanto você estava sem internet.

---

### 13. `git restore` — Desfazer mudanças

```bash
# Desfazer mudanças em um arquivo (antes de adicionar com git add)
git restore nome-do-arquivo.txt

# Tirar um arquivo da fila do git add
git restore --staged nome-do-arquivo.txt
```

**O que faz:** Descarta as mudanças feitas em um arquivo e volta ele para como estava no último commit.

> 💡 É o "Ctrl+Z" do Git! Cometeu um erro? Use esse comando para voltar ao estado anterior.

---

### 14. `git revert` — Desfazer um commit com segurança

```bash
git revert abc1234
```

**O que faz:** Cria um novo commit que desfaz as mudanças de um commit anterior. É a forma mais segura de "voltar no tempo" porque não apaga o histórico.

> 💡 O código `abc1234` é o identificador do commit — você consegue ele com o `git log --oneline`.

---

### 15. `git stash` — Guardar mudanças temporariamente

```bash
# Guardar as mudanças atuais
git stash

# Recuperar as mudanças guardadas
git stash pop
```

**O que faz:** Coloca suas mudanças "na gaveta" temporariamente, sem commitar. Útil quando você precisa trocar de branch mas não quer perder o que estava fazendo.

> 💡 É como guardar o rascunho de uma redação na gaveta para fazer outra coisa, e depois continuar de onde parou.

---

## 🔄 Fluxo de trabalho no dia a dia

Agora que você conhece os comandos, veja como eles se encaixam na rotina:

```
1. git pull           → Atualiza o projeto com as novidades do GitHub
2. (edita os arquivos)
3. git status         → Confere o que mudou
4. git add .          → Coloca tudo na fila
5. git commit -m "..."→ Salva a versão com uma mensagem
6. git push           → Envia para o GitHub
```

---

## 🧠 Resumo rápido

| Comando | Para que serve |
|---|---|
| `git init` | Inicia um repositório |
| `git clone <url>` | Copia um projeto do GitHub |
| `git status` | Vê o que mudou |
| `git add .` | Adiciona tudo na fila |
| `git commit -m ""` | Salva uma versão |
| `git log --oneline` | Vê o histórico |
| `git diff` | Vê o que mudou linha a linha |
| `git branch` | Gerencia branches |
| `git merge` | Junta branches |
| `git push` | Envia para o GitHub |
| `git pull` | Baixa do GitHub |
| `git restore` | Desfaz mudanças |
| `git stash` | Guarda mudanças temporariamente |

---

> 🚀 **Dica final:** O segredo para aprender Git é **praticar**! Crie um repositório de teste no GitHub e experimente todos esses comandos sem medo de errar. O Git foi feito justamente para que você possa errar e voltar atrás com facilidade!
