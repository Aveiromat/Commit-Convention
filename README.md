# 🛡️ Padrões de commits e Validador (Git Hook) 📜

Este repositório é uma **ferramenta auxiliar** criada para ser utilizada em vários tipos de projetos. Ele contém:
1. Um script `commit-msg` (Git Hook personalizado) para garantir que qualquer projeto siga estritamente o padrão de **Conventional Commits com Emojis**.
2. A documentação completa das regras no arquivo `COMMIT_CONVENTION.md`.

## 📖 Regras de Commits

Para conferir todas as regras, tipos de commits (feat, fix, chore, etc.), lista de emojis e comandos úteis do Git, consulte o documento oficial:

👉 **[Ler as Regras de Commits (COMMIT_CONVENTION.md)](./COMMIT_CONVENTION.md)**

---

## 🛠️ Como utilizar este repositório em OUTROS Projetos Novos

Como este é um repositório auxiliar, o objetivo é levar a pasta `.githooks` e o arquivo `COMMIT_CONVENTION.md` para os seus novos projetos e configurá-lo para validar as mensagens de commit localmente.

### Passo 1: Obtenha os arquivos 📂

Copie a pasta `.githooks` e o arquivo `COMMIT_CONVENTION.md` deste repositório para a raiz do seu novo projeto.

Por exemplo:
```bash
# Clone este repositório auxiliar em algum lugar
git clone https://github.com/Aveiromat/Commit-Convention.git

# Copie os arquivos de configuração para a raiz do seu projeto novo
cp -r Commit-Convention/.githooks /caminho/para/seu/novo-projeto/
cp Commit-Convention/COMMIT_CONVENTION.md /caminho/para/seu/novo-projeto/
```

### Passo 2: Configure o Git para usar a pasta `.githooks` ⚙️

No terminal, navegue até a raiz do seu novo projeto. O Git, por padrão, procura hooks na pasta oculta `.git/hooks`. Para podermos versionar nossos scripts no GitHub, configuraremos o Git para olhar para a nova pasta `.githooks`:

```bash
cd /caminho/para/seu/novo-projeto/
git config core.hooksPath .githooks
```

### Passo 3: Garanta que o script tem permissão de execução ✅

Para que o Git consiga executar o hook:

```bash
chmod +x .githooks/commit-msg
```

### Passo 4: Teste o hook de commit 💻

Faça um commit de teste:

```bash
git add .
git commit -m "feat: adicionar funcionalidade xyz"
```

Se a mensagem não possuir um emoji e um tipo válido (ex: `✨ feat: `), o terminal bloqueará o commit e exibirá as instruções corretas baseadas no `COMMIT_CONVENTION.md`.

> **Nota:** Commits automáticos de Merge (ex: `Merge branch...`) são ignorados para não impactar o fluxo de trabalho do Git.
