<div align="center">
  
# 🛡️ Padrões de Commits e Validador (Git Hook) 📜

[![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg)](https://conventionalcommits.org/pt-br)
[![Git Hook](https://img.shields.io/badge/Git-Hooks-F05032?logo=git)](https://git-scm.com/docs/githooks)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

**Ferramenta auxiliar para padronização automática de commits em múltiplos projetos.**

</div>

---

## 🎯 Sobre o Projeto

Este repositório é uma **ferramenta auxiliar** criada para ser facilmente acoplada a outros projetos novos ou já existentes. O objetivo principal é automatizar e _forçar_ o padrão de **Conventional Commits com Emojis** através de um script de **Git Hook** (`commit-msg`).

A estrutura contém:
1. 🛡️ **Script `commit-msg`**: O "segurança" que valida as mensagens antes que o commit seja registrado no Git.
2. 📖 **Regras e Convenções**: Toda a documentação organizada no arquivo `README.md` dentro da pasta de hooks.

---

## 💡 Como os commits devem ficar?

Antes do script permitir que um commit seja salvo no seu projeto, ele verifica a obrigatoriedade da estrutura: `<Emoji> <tipo>: <descrição>`. 

Abaixo estão alguns exemplos de **commits válidos** e aceitos:

- `✨ feat: adiciona tela de dashboard do usuário`
- `🐛 fix: corrige erro de autenticação no login`
- `♻️ refactor: melhora performance da listagem de itens`
- `📚 docs: atualiza as instruções de configuração`
- `🚀 deploy: publica versão v2.1.0 na produção`

---

## � Onde ler as Regras de Commits?

Para conferir todas as regras, tipos de commits (feat, fix, chore, etc.), lista de emojis e comandos úteis do Git, consulte a documentação oficial da ferramenta, contida na pasta `.githooks` deste repositório:

👉 **[Acessar Regras de Commits e Emojis 📚](./.githooks/README.md)**

---

## 🚀 Como instalar em meus projetos?

A instalação é **extremamente rápida** e foi desenhada no estilo _plug-and-play_. Você precisa apenas copiar a pasta de hooks deste repositório para o seu e rodar breves comandos.

### 1️⃣ Obtenha a pasta `.githooks`

Copie a pasta oculta chamada `.githooks` deste repositório para a **raiz** do seu novo projeto. Tudo o que é necessário (o script Bash e a documentação completa) já está dentro dela!

```bash
# Clone este repositório auxiliar em algum local temporário:
git clone https://github.com/Aveiromat/Commit-Convention.git

# Copie a pasta inteira para o seu projeto destino:
# Substitua "/caminho/para/o/seu/projeto/" pelo caminho real da sua aplicação.
cp -r Commit-Convention/.githooks /caminho/para/o/seu/projeto/
```

<br>

### 2️⃣ Configure e Ative o Hook

As instruções finais (super rápidas) de como configurar o seu Git local (dando as permissões pro script e mandando o Git ler a pasta) estão documentadas direto na fonte:

👉 **[Ler os passos de ativação ⚙️](./.githooks/README.md)**

---

<br>

<div align="center">
  <small>💡 <b>Dica pro time:</b> Commits automáticos de Merge (ex: <code>Merge branch...</code>) são inteligentemente ignorados pelo nosso script para não quebrar o fluxo de trabalho natural dos pull requests!</small>
</div>
