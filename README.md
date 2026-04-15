# Aula Prática Git: Meu Primeiro Commit Profissional

**Repositório da turma:** `https://github.com/rlzambroti/aula20260414`
**Data:** 07/04/2025  

> Utilize o material teórico disponibilizado pelo professor para consultar [aqui](guia_git_iniciantes.md)
> os comandos necessários. O objetivo é que você **encontre e execute**
> cada comando, não apenas copie uma resposta pronta.

---

## Antes de começar

Verifique se o Git está instalado na sua máquina e se você já tem uma
conta no GitHub. Caso ainda não tenha configurado sua identidade no Git
(nome e e-mail), faça isso antes de iniciar os exercícios — sem essa
configuração o Git não permite realizar commits.

---

## Exercício 01 — Configure sua identidade no Git

O Git precisa saber quem está fazendo as alterações antes de permitir
qualquer commit. Configure seu **nome completo** e seu **e-mail** nas
configurações globais do Git na sua máquina.

Após configurar, verifique se as informações foram salvas corretamente
listando todas as configurações ativas do Git.

> 💡 Consulte no material: seção sobre configuração inicial do Git.

---

## Exercício 02 — Clone o repositório da turma

Faça uma cópia local do repositório da turma na sua máquina. Após
clonar, entre na pasta do repositório pelo terminal.

Verifique em qual branch você está e quantos commits já existem no
histórico do repositório.

> 💡 Consulte no material: seção sobre repositórios remotos e o comando clone.

---

## Exercício 03 — Crie sua branch pessoal

Crie uma nova branch seguindo **obrigatoriamente** o padrão abaixo e já
mude para ela:

```
aluno/seuprimeironome-seuRA
```

Exemplos válidos: `aluno/joao-123456` · `aluno/maria-654321`  
Exemplos **inválidos**: `aluno/JoaoSilva` · `joao-123456` · `aluno/joao`

Após criar, confirme que você está na branch correta antes de continuar.

> 💡 Consulte no material: seção sobre branches — criação e navegação.

---

## Exercício 04 — Crie seu arquivo de identificação

Dentro da pasta `alunos/`, existe um arquivo chamado `MODELO.md`.
Faça uma cópia dele e renomeie para `seuprimeironome-seuRA.md`
(o mesmo identificador usado no nome da sua branch).

Após criar o arquivo, use o comando adequado para verificar o estado
atual do repositório — o Git deve mostrar que existe um arquivo novo
ainda não rastreado.

Adicione **apenas este arquivo** à área de preparação (staging area) e
realize o primeiro commit com uma mensagem seguindo o padrão:

```
docs: cria cartão de identidade de seuprimeironome-seuRA
```

Envie sua branch para o repositório remoto.

> 💡 Consulte no material: seções sobre `git status`, `git add`, `git commit` e `git push`.

---

## Exercício 05 — Preencha seus dados pessoais

Abra o arquivo que você criou no exercício anterior e preencha
**todos os campos** da tabela de identificação:

- Nome completo
- RA (número de registro acadêmico)
- Turma
- Email
- WhatsApp no formato `55` + DDD + número (ex: `5544999998888`)
- Sistema operacional que você está usando

> ⚠️ O campo Email é obrigatório para você receber o feedback
> desta aula. Preencha no formato correto.

Após preencher, adicione o arquivo à staging area e realize o segundo
commit com uma mensagem padronizada descrevendo o que foi feito.
Envie para o repositório remoto.

> 💡 Consulte no material: boas práticas para mensagens de commit.

---

## Exercício 06 — Pratique o comando de desfazer alterações

Faça qualquer alteração no seu arquivo `.md` — pode ser adicionar uma
linha qualquer ou modificar algo existente.

Sem fazer commit, use o comando correto para **descartar completamente**
essa alteração e deixar o arquivo exatamente como estava no último
commit.

Verifique com o `git status` que o arquivo voltou ao estado anterior.

> 💡 Consulte no material: seção sobre como desfazer alterações no
> diretório de trabalho.

---

## Exercício 07 — Preencha a seção de aprendizados e consulte o histórico

Abra novamente seu arquivo `.md` e preencha a seção
**"O que aprendi hoje"** com pelo menos três frases descrevendo
o que você aprendeu nesta aula prática.

Realize o terceiro e último commit com uma mensagem padronizada
e envie para o repositório remoto.

Por fim, consulte o histórico de commits da sua branch de duas formas:
- De forma resumida, com uma linha por commit
- Com a representação gráfica das branches

Identifique o **hash** do seu primeiro commit e anote — o professor
pode pedir durante a aula.

> 💡 Consulte no material: seção sobre `git log` e suas opções.

---

## Critérios avaliados automaticamente ao final da aula

Ao concluir todos os exercícios, você receberá um feedback automático
no WhatsApp com o resultado de cada item abaixo:

| # | O que será verificado |
|---|-----------------------|
| 1 | Branch criada no padrão `aluno/nome-ra` |
| 2 | Mínimo de 3 commits realizados na branch |
| 3 | Todas as mensagens de commit com prefixo válido (`feat:`, `docs:`, `fix:`, etc.) |
| 4 | Arquivo `alunos/seunome-ra.md` criado e enviado |
| 5 | Todos os campos da tabela preenchidos (sem placeholders `[...]`) |
| 6 | WhatsApp cadastrado no formato correto |
| 7 | Seção "O que aprendi hoje" preenchida com conteúdo |

---

*Dúvidas durante a aula? Chame o professor.*